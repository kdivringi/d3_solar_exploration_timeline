#A Visualization of Solar System Exploration

*By Kaan Divringi*

*Udacity Final Project - Make Effective Data Visualization*

[Link to live visualization](http://kdivringi.github.io/)

##Summary

This visualization is an interactive, re-imagined version of [this](https://commons.wikimedia.org/wiki/File:Timeline_of_Solar_System_exploration.jpg) infographic, a timeline of solar exploration missions in the space age. The intent was to present as much of the information from the original graphic as possible in a more accessible way, taking advantage of the interactivity that D3 enables.

##Design

My first design decision was to place the time axis on the horizontal axis, taking advantage of a well established convention in line charts so that the user can more intuitively grasp the chart.

One of the difficulties I found in the original chart was identifying locations. It was not always easy to match the color to the location in the legend and often necessitated zooming in and out many times, especially when the color was ambiguous. In extracting the colors I actually used a color picker tool in a paint program. I decided to make the color areas regular and have bands labeled right on the axis instead of in a separate legend. This, in my opinion, conveys the two most important variables of the chart (time and location) using the two most powerful visual indicators: position x and y. Because of the ordinal nature of the vertical position labels, I added the bands of color from the original graphic to strengthen this indicator.

Because of the need to compress the larger infographic into a smaller area, some information was left out of the default view. A mouse over of the lines can get an info-box of more information on the missions. In the zoomed-in view of any of the locations the mission names are added, as will symbols for the mission type (work in progress). The default view does convey time, position, mission stages and mission success/failure for all of the missions at once without any zooming needing.

The secondary destinations information from the original graph was not added, due to the complexity it would have created. This ended up reducing the total number of locations, however, as some locations were not the primary destination for any of the missions. This ended up making the overall graph still easier to read. I also did not deal with unusual mission sequences, such as the trip-activity-trip of the Dawn mission in the original graphic. Every mission in this graphic has one trip and then one activity period.

Overall I believe I was able to represent the original graphic in a more accessible way. General patterns are observable and the outlines of the story of our exploration missions in the solar system are shown.


##Feedback

Feedback1:
Nice project...

>The visualisation immediately shows which areas/planets of the solar system were more intensely explored.
>
>Also - the time axis instantly shows how long some classes of missions take compared to others... Interactive popup detail info is a nice touch. On my display the dark blue caption blends into the black popup background, perhaps you can try a lighter color heading.
>
>The  mission type "Flyby", "Lander" etc. may be overloaded into the graphic as a line color?
>
>The main takeaway is the instant visualization of how some destinations, such as Mars and Sun are getting increased attention in sheer number of missions aimed at them.  
>
>I think the visualization is effective but can be improved with a couple minor tweaks if possible:
>- Graph-paper like vertical faint lines delineating years would be helpful
>- Horizontal colors delineating planets is nice but Jupiter and Saturn mix together - altering that selection would be helpful.
>- Links in the text are indistinguishable. Just making them bold and blue may help. 
>- Bulleted list for the points made after the graphic, perhaps?

Feedback2:
>Congrats on your progress!
>
>1. It says click on the right text locations to zoom in, it may say click on the left planet names to zoom in.
>
>2. I believe legend is missing an item or two, like the type of mission, success vs failure (I looked into the infographic referenced)
>
>Answers to suggested questions:
>What do you notice in the visualization?
>- There is clear interest in Mars. Venus used to be center of interest in past decades but not any more. 
>
>What questions do you have about the data?
>- Why is there a lot of failed projects/trips to Mars? And yet there is still a lot of interest.
>
>What relationships do you notice?
>- Could not really read this part well from the interactive chart.
>
>What do you think is the main takeaway from this visualization?
>- Mars has been and currently is the main destination for human space/solar system exploration
>
>Is there something you don’t understand in the graphic?
>- I did not really understand the dashed line part showing the trips. Is not it the case that all trips start off from earth? Why does some trips has this dashed line part.

Feedback3:
>I'd like to see colors specific to the planet in each section. Over the word SUCCESS I'd like to see a short starburst when you mouse over it. Extras would include a small picture of the planet when you mouse over the planet's name.
>
>There should be a space after chart: " chart(time and location)"
>
>I find it much easier to visualize this compared to the original. This allows for a 3d time and space representation. Due to the way the graph flows I can picture the object moving outward - colors will have add the extra bonus of space temperature visualization.
>
>The model also takes up less space and is more easily read.

### Design Re:Feedback

Feedback for the visualization was generally positive. One person suggested adding mission types to the visualization, which I already had in mind and had partly started. I ended up creating some original svg graphics for each one in Inkscape and adding them in programmatically. The mission type icons are too much detail in the overall view but when it is zoomed in they are added, along with a legend to the left to denote the types. The legend is too distracting on the global view so I decided to show it only in the zoomed in view.

I redid the planet/location colors on the suggestion of two of the reviewers. While I couldn't really find one iconic color for each location (many of them are grey or brown, mostly) I used a qualitative color schema from ColorBrewer2 and matched some of the colors appropriate to some of the more popular locations. The premade palette avoids the trouble of distinguishing some of the colors from each other, which was one of the comments.

Faint vertical lines were added, as requested. It was important to make these faint enough so they did not make an already busy chart too busy.

The links in the explanatory text were made bold to make them easier to see.

I added some explanation below the legend as to why not every mission has a trip line from the Earth location. That is something that can be difficult to grasp, especially if the mission type data is not as easily seen as it is now.

##Resources

- http://www.svgbasics.com/markers.html
- http://vanseodesign.com/web-design/svg-markers/
- http://alignedleft.com/tutorials/d3/axes
- http://bl.ocks.org/mbostock/1166403
- https://github.com/mbostock/d3/wiki
- http://bl.ocks.org/WilliamQLiu/76ae20060e19bf42d774
- http://getbootstrap.com/css/
- http://www.w3schools.com/svg/svg_path.asp
- https://en.wikipedia.org/wiki/Timeline_of_Solar_System_exploration
- https://developer.mozilla.org/en-US/docs/Web/SVG/Attribute/text-anchor
- https://s3.amazonaws.com/udacity-hosted-downloads/ud507/Canvas_and_Axes.jpeg
- http://colorbrewer2.org/