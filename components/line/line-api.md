<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

### Table of Contents

-   [LINE_DEFAULTS](#line_defaults)
-   [Line](#line)
    -   [updated](#updated)
    -   [destroy](#destroy)
-   [rendered](#rendered)

## LINE_DEFAULTS

**Properties**

-   `dataset` **[array](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array)** The data to use in the line/area/bubble.
-   `tooltip` **([function](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/function) \| [string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String))** A custom tooltip or tooltip renderer function
    for the whole chart.
-   `isArea` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** Render as an area chart.
-   `isBubble` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** Render as a bubble chart.
-   `showLegend` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** If false the label will not be shown.
-   `xAxis` **[object](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object)** A series of options for the xAxis
    -   `xAxis.rotate` **[number](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Number)** Rotate the elements on the x axis.
        Recommend -65 deg but this can be tweaked depending on look.
    -   `xAxis.ticks` **[object](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object)** Data to control the number of ticks and y axis format.
        For example `{number: 5, format: ',.1s'}` would show only 5 yaxis points and format the
        data to show 1K, 1M, 1G ect.. This uses the d3 formatter.
    -   `xAxis.formatText` **[function](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/function)** A function that passes the text element and a counter.
        You can return a formatted svg markup element to replace the current element.
        For example you could use tspans to wrap the strings or color them.
-   `yAxis` **[object](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object)** A series of options for the yAxis
    -   `yAxis.formatter` **[function](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/function)** A d3 formatter for the yAxis points.
-   `yAxis` **[object](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object)** A series of options for the yAxis
-   `hideDots` **[boolean](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean)** If true no dots are shown
-   `axisLabels` **[array](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array)** Option to a label to one of the four sides. For Example
    `{left: 'Left axis label', top: 'Top axis label',
    right: 'Right axis label', bottom: 'Bottom axis label'}`
-   `animate` **([boolean](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean) \| [string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String))** true|false - will do or not do the animation.
    'initial' will do only first time the animation.
-   `redrawOnResize` **[boolean](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Boolean)** If true, the component will not resize when resizing the page.
-   `dots` **[object](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object)** Option to customize the dot behavior. You can set the dot size (radius),
    the size on hover and stroke or even add a custom class.
    Example `dots: { radius: 3, radiusOnHover: 4, strokeWidth: 0, class: 'custom-dots'}`
-   `formatterString` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** Use d3 format some examples can be found on <http://bit.ly/1IKVhHh>
-   `emptyMessage` **[object](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object)** An empty message will be displayed when there is no chart data.
    This accepts an object of the form emptyMessage:
    `{title: 'No Data Available',
     info: 'Make a selection on the list above to see results', icon: 'icon-empty-no-data',
     button: {text: 'xxx', click: <function>}
     }`
     Set this to null for no message or will default to 'No Data Found with an icon.'

## Line

A line chart or line graph is a type of chart which displays information as a series of data
points called 'markers' connected by straight line segments.

**Parameters**

-   `element` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** The plugin element for the constuctor
-   `settings` **[string](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/String)** The settings element.

### updated

Handle updated settings and values.

**Parameters**

-   `settings` **[object](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object)** The new settings to use.

Returns **[object](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object)** The api for chaining.

### destroy

Remove added markup and events.

Returns **void** 

## rendered

Fires when the chart is complete done rendering, for customization.

**Properties**

-   `event` **[object](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Object)** The jquery event object
-   `svg` **[array](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array)** The svg object.