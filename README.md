A collection of demonstrations of bugs in certain browsers. Status should be fairly up-to-date.

Visit here for easy viewing of demos: [bitbof.github.io/browser-bug-demos](https://bitbof.github.io/browser-bug-demos/)

# <span style="color:red">Not Fixed</span>

## Chrome
<table>
<thead>
    <tr>
        <th>Date</th>
        <th>Live Demo</th>
        <th>Summary</th>
        <th>Effects</th>
        <th>Issue Link</th>
    </tr>
</thead>
<tr>
    <td>2021-02-15</td>
    <td><a href="2021-02-15-chrome-iframe-pointerid-bug">View</a></td>
    <td>In an iframe, when using a stylus, PointerEvent.pointerId is inconsistent.</td>
    <td>Drawing applications can't reliably run in iframes. I.e. Kleki/Klecks can't be easily embedded via iframe.</td>
    <td><a href="https://bugs.chromium.org/p/chromium/issues/detail?id=1178643">Chromium Ticket</a> (reported 2021-02-15)</td>
</tr>
<tr>
    <td>2022-04-28</td>
    <td><a href="2022-04-28-chrome-intelhd400-canvas">View</a></td>
    <td>CanvasRenderingContext2D deletes parts of image after switching tabs.</td>
    <td>With certain hardware, drawing apps or image editing apps can't reliably run, as image data gets corrupted, when switching tabs. I.e. Kleki/Klecks users lose progress.</td>
    <td><a href="https://bugs.chromium.org/p/chromium/issues/detail?id=1309876">Chromium Ticket</a> (reported 2022-03-24)</td>
</tr>
<tr>
    <td>2022-10-19</td>
    <td><a href="2022-10-19-chrome-arc">View</a></td>
    <td>Context2d arc() fill() draws jagged circles on MacOS M1.</td>
    <td>Applications relying on the canvas arc method achieve bad quality circles. I.e. the pen tool in Kleki/Klecks looks much worse.</td>
    <td><a href="https://bugs.chromium.org/p/chromium/issues/detail?id=1377687">Chromium Ticket</a> (reported 2022-10-23)</td>
</tr>
</table>

## Safari
<table>
<thead>
    <tr>
        <th>Date</th>
        <th>Live Demo</th>
        <th>Summary</th>
        <th>Effects</th>
        <th>Issue Link</th>
    </tr>
</thead>
</table>

## Firefox
<table>
<thead>
    <tr>
        <th>Date</th>
        <th>Live Demo</th>
        <th>Summary</th>
        <th>Effects</th>
        <th>Issue Link</th>
    </tr>
</thead>
<tr>
    <td>2022-03-08</td>
    <td><a href="2022-03-08-firefox-pointer-buttons">View</a></td>
    <td>PointerEvent.buttons attribute is inconsistent when using a stylus.</td>
    <td>Drawing applications break, unless they handle Firefox differently (not trust the button attribute).</td>
    <td><a href="https://bugzilla.mozilla.org/show_bug.cgi?id=1758516">Bugzilla Ticket</a> (reported 2022-03-08)</td>
</tr>
</table>

# todo
- chrome invert artifacts https://github.com/bitbof/klecks/issues/8
- safari canvas gradient -> webgl glitch https://github.com/bitbof/klecks/issues/41
- safari canvas duplication glitch https://github.com/bitbof/klecks/issues/68
- chrome disappearing cursor with pen (need demo?)
- firefox text repositioning after scrolling



