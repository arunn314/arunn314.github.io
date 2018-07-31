---
layout: project
type: project
image: images/micromouse.jpg
title: Micromouse
published: false
permalink: projects/micromouse
# All dates must be YYYY-MM-DD format!
date: 2015-07-01
labels:
  - Robotics
  - Arduino
  - C++
summary: My team developed a robotic mouse that won first place in the 2015 UH Micromouse competition.
---

<div class="ui small rounded images">
  <img class="ui image" src="../images/micromouse-robot.png">
  <img class="ui image" src="../images/micromouse-robot-2.jpg">
  <img class="ui image" src="../images/micromouse.jpg">
  <img class="ui image" src="../images/micromouse-circuit.png">
</div>

Micromouse is an event where small robot “mice” solve a 16 x 16 maze.  Events are held worldwide.  The maze is made up of a 16 by 16 gird of cells, each 180 mm square with walls 50 mm high.  The mice are completely autonomous robots that must find their way from a predetermined starting position to the central area of the maze unaided.  The mouse will need to keep track of where it is, discover walls as it explores, map out the maze and detect when it has reached the center.  having reached the center, the mouse will typically perform additional searches of the maze until it has found the most optimal route from the start to the center.  Once the most optimal route has been determined, the mouse will run that route in the shortest possible time.

For this project, I was the lead programmer who was responsible for programming the various capabilities of the mouse.  I started by programming the basics, such as sensor polling and motor actuation using interrupts.  From there, I then programmed the basic PD controls for the motors of the mouse.  The PD control the drive so that the mouse would stay centered while traversing the maze and keep the mouse driving straight.  I also programmed basic algorithms used to solve the maze such as a right wall hugger and a left wall hugger algorithm.  From there I worked on a flood-fill algorithm to help the mouse track where it is in the maze, and to map the route it takes.  We finished with the fastest mouse who finished the maze within our college.

Here is some code that illustrates how we read values from the line sensors:

```js
byte ADCRead(byte ch)
{
    word value;
    ADC1SC1 = ch;
    while (ADC1SC1_COCO != 1)
    {   // wait until ADC conversion is completed   
    }
    return ADC1RL;  // lower 8-bit value out of 10-bit data from the ADC
}
```

```python

    {
      "company": "Machine Zone Inc., CA, USA",
      "position": "Research Scientist",
      "website": "",
      "startDate": "2012-07-02",
      "endDate": "2018-05-11",
      "summary": "",
      "highlights": [
"Used    Faster RCNN    Model   in  Tensorflow  for object  detection   for extracting  attributes  in  Image   Assets. ",
"Measuring   Install lift    from    TV  Marketing   Campaigns   for Game    of  War,    Mobile  Strike  games.  ",
"TV  Ads Attribution model   to  attribute   installs    to  TV  spots   (Patent 4). ",
"ML  based   Feature Recommendation  for Video   Ads to  boost   performance for Mobile  Strike. ",
"Launch/manage   Facebook    Retargeting Campaigns   using   FBAds   API.    ",
"ML  based   scoring model   for Google  Text    ads to  decide  whether to  pause   underperforming ads.    ",
"Correct For Rewards -   Built   in-game mechanical  turk    to  make    users   correct errors  in  machine translations    (Patent 1). ",
"Translation  Correction - Built NLP system to automatically validate whether two messages in two different languages (10+ languages)  mean    the same    with    high    accuracy    (Patent 2). ",
"Emoji   Suggestion  -   Suggest emoji   in  real    time    as  the user    types   in  some    message (Patent 3). ",
"Analyze Trending    Topics  in  game    chats   using   Scalding.   ",
"Built   a   search  engine  for game    chat    messages    from    Kafka   using   ElasticSearch."
      ]
    },
```

You can learn more at the [UH Micromouse Website](http://www-ee.eng.hawaii.edu/~mmouse/about.html).



