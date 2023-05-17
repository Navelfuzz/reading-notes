# Class 12 Readings: Chart.js, Canvas

## [JavaScript Canvas](https://www.javascripttutorial.net/web-apis/javascript-canvas/)

*Questions*

1. What does the `<canvas>` allow a developer to acheive?
2. What is the importance of the closing `</canvas>` tag?
3. Explain what the `getContext()` method does.

*Answers*

1. Allows you to draw 2d graphics using JS
2. Allows you to fill the tags with fallback content in the case that the browser doesn't support the feature.

## [Chart.js Documentation:](https://www.chartjs.org/docs/latest/)

*Questions*

1. What is Chart.js and how it can be brought into your project?
2. List 3 different Chart types you can create using Chart.js.

*Answers*

1. it's a means to bring dynamic charts to your website. Integrated with many JS frameworks and is used via the `<script>` tag.

        <script src="path/to/chartjs/dist/chart.umd.js"></script>
        <script>
            const myChart = new Chart(ctx, {...});
        </script>

2. Area, Bar, Bubble, Doughnut/Pie, Line, Mixed, Polar, Radar, Scatter

## [Easily Create Stunning Animated Charts with Chart.js](https://www.webdesignerdepot.com/2013/11/easily-create-stunning-animated-charts-with-chart-js/)

*Questions*

1. What are some advantages to displaying data via a chart over a table?
2. How could Chart.js aid your previously created applications visually?

*Answers*

1. You can animate, provide dynamic viewing features (such as zoom), and choose various display methods i.e. table, pie chart, line graph.
2. Give visual representation to data in a more exciting way.

### Bookmark and Review

[Drawing Shapes With Canvas](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_shapes)

[Applying Style and Colors - Canvas API](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Applying_styles_and_colors)

[Drawing Text - Canvas API](https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_text)
