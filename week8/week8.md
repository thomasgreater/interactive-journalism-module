Interactive Journalism - Advanced Data & Coding module
========================================================

Module code: JOM299

Charting for the webz: alternatives to d3.js

"You may not need d3"
========================================================

Jerome Cukier, dataviz designer at Facebook

http://www.jeromecukier.net/blog/2015/05/19/you-may-not-need-d3/

(advanced knowledge of d3 ins and outs required)

"You may not need d3"
========================================================

In short:

* You can manipulate the DOM and styles without d3 (that's HTML/CSS and Javacscript selectors)
* Loading data in d3 can be replaced with XHR requests
* You can replace data joins, even if nazis say you can't
* Animations can be replaced by keyframes
* But d3 has loads of helped and shortcuts

========================================================

# But crucially

d3 is **hard**

You have to set up:
* Your own canvas/ SVG container
* Your axis and their domain and extent
* The way you want to represent your data

========================================================

There are few helpers to guide you!

You chart is nothing more than DOM elements you throw on a canvas.

- A bar chart is rectangles of varied heights placed along an x-axis
- A scatterplot is a bunch of elements with x/y coordinates
- Areas must be calculated manually
- And so must angles
- X/Y depend on your scales: linear? timeseries? logarithmic?

An alternative: Highcharts
========================================================

http://www.highcharts.com/products/highcharts

![](img/highcharts.png)

Highcharts
========================================================

* Works everywhere + responsive
* License is free for non-commercial
* Many chart types and documented examples
* Syntax is configuration-oriented
* Handles tooltips, date axis...
* Export charts as images or SVG for embed
* And probably much more...

A first chart
========================================================

http://www.highcharts.com/docs/getting-started/your-first-chart

What you need:

* An HTML `<div>`
* Some Javascript instantiating a charts on your `<div>`

Example:

http://jsfiddle.net/highcharts/kh5jY/

========================================================

```
    $('#container').highcharts({
        series: [{
            type: 'bar',
            data: [5, 7, 3]
        }]
    });
```

![](img/bar.png)

http://jsfiddle.net/43tnpxc6/

========================================================

![](http://i.imgur.com/YsbKHg1.gif)

Some vocabulary
========================================================

![](http://www.highcharts.com/images/docs/understanding_highcharts.png)

_Image source: Highcharts.com_

Options
========================================================

http://www.highcharts.com/docs/getting-started/how-to-set-options

Javascript objects?!?

![](img/obj.png)

Image source: https://www.w3schools.com/js/js_objects.asp

Series = your chart data
========================================================

http://www.highcharts.com/docs/chart-concepts/series

Should remind you of lists and objects:

```
[1, 2, 10, 42]
```

```
{
    name: 'Point 1',
    y: 0
},{
    name: 'Point 2',
    y: 5
}
```

Chart types
========================================================

Highcharts allow you to build all kinds of charts: 

http://www.highcharts.com/docs/chart-and-series-types/chart-types

Using `series`, we can combine chart types, eg a bar chart with a line on top:

http://jsfiddle.net/gh/get/library/pure/highcharts/highcharts/tree/master/samples/highcharts/demo/combo/

Demos
========================================================

http://www.highcharts.com/demo

Your turn
========================================================

* Simple bar chart: http://jsfiddle.net/0nsqbr03/
* Simple area chart: http://jsfiddle.net/kLgoq9vs/
* Complex x/y heatmap: http://jsfiddle.net/etbx3L20/

Another alternative: Chart.js
========================================================

http://www.chartjs.org/

![](img/chartjs.png)

Example: a doughnut chart
========================================================

http://jsfiddle.net/achudars/NXPhL/

```
var data = [...];
var options = { animations: false };

var context = $('#myChart').get(0).getContext('2d');

myNewChart = new Chart(context).Doughnut(data, options);
```

========================================================

http://jsfiddle.net/jsanz/uLUAT/

https://jsfiddle.net/milostimotic/e8n4xd4z/


Graphical alternatives
========================================================

https://plot.ly/create/

https://quartz.github.io/Chartbuilder/

NEXT WEEK
========================================================

#Final project group work

Bring your ideas, your questions, your code, and your creativity
