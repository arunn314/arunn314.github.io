---
layout: project
type: project
image: images/expenses.jpg
title: Track Expenses by Categories
permalink: projects/expenses_alert

date: 2017-07-14
labels:
  - Redis
  - Plaid API
  - Raspberry Pi

summary: Raspberry Pi based chatbot to visualization of expenses by category per week/month.
---
It is hard for us to track expenses we make everyday. There are apps like mint to help us set budgets under each category like Food, Groceries, ATM, Pharmacy etc. However, I thought I would make my chatbot to track my expenses, send me alerts when I exceed the weekly budget and send me a visual report of what percentage of my expenses go into what categories.<br/>

I found Plaid API suitable to track my expenses. The development mode is free and it can track upto 5 accounts. I connected my Credit and debit card account to Plaid API and everything is set. My chatbot queries the API every 15 minutes and stores them in a Redis Cache in Raspberry Pi.<br/>

Budget limits are set in the code for each category. Chatbot has a category map which you can find in my code can be used to map expenses to their correponding category. The list is not exhaustive and new categories can be added.<br/>

Whenever, Plaid API returns new expenses, chatbot classifies the expense into one of the available categeories and checks if the total expenses in the current week exceed the budget allocated for a category. If it exceeds, chatbot sends me alert in FB messenger saying an expense exceed the budget.<br/>
<img class="ui medium center floated rounded image" src="../images/expenses_alert.png"><br/>

Every week on sunday, the chatbot sends me a cool visualization of what percent of expenses go into what category. The following is a sample pie chart of one week of my expenses. The bot also sends monthly expenses visualization on the last day of every month.<br/>
<img class="ui medium right floated rounded image" src="../images/expenses_pie.png"><br/>

I can also ask questions like "How much did I spend on food last 2 weeks ?". The bot will respond with a list of expenses under the food category in the last 2 weeks.<br/>
[Plaid API code](https://github.com/arunn314/smartybot/blob/master/plaid_handler.py)<br/>
[Expense tracking Code](https://github.com/arunn314/smartybot/blob/master/expenses_server.py)<br/>
