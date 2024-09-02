This repo demonstrates some browser bugs that tend to affect drawing web apps the most. Status should be fairly up-to-date.

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
    <td>Drawing applications can't reliably run in iframes. I.e. Kleki/Klecks can't be embedded via iframe without glitching.</td>
    <td><a href="https://bugs.chromium.org/p/chromium/issues/detail?id=1178643">Chromium Ticket</a> (reported 2021-02-15)</td>
</tr>
<tr>
    <td>2022-04-28</td>
    <td><a href="2022-04-28-chrome-intelhd400-canvas">View</a></td>
    <td>CanvasRenderingContext2D deletes parts of image after switching tabs.</td>
    <td>With certain hardware, drawing apps or image editing apps aren't reliable, as image data gets corrupted when switching tabs. I.e. Kleki/Klecks users lose progress.</td>
    <td><a href="https://bugs.chromium.org/p/chromium/issues/detail?id=1309876">Chromium Ticket</a> (reported 2022-03-24)</td>
</tr>
<tr>
    <td>2022-10-19</td>
    <td><a href="2022-10-19-chrome-arc">View</a></td>
    <td>Context2d arc() fill() draws jagged circles on MacOS M1.</td>
    <td>Applications relying on the canvas arc method achieve bad quality circles. I.e. the pen tool in Kleki/Klecks looks much worse.</td>
    <td><a href="https://bugs.chromium.org/p/chromium/issues/detail?id=1377687">Chromium Ticket</a> (reported 2022-10-23)</td>
</tr>
<tr>
    <td>2024-06-23</td>
    <td>no demo</td>
    <td>Cursor disappears with Windows Ink</td>
    <td>Seeing no cursor worsens visual feedback for stylus users.</td>
    <td><a href="https://issues.chromium.org/issues/348869917">Chromium Ticket</a> (reported 2024-06-23)</td>
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
<tr>
    <td>2024-09-02</td>
    <td><a href="2024-09-02-safari-mac-escape-key">View</a></td>
    <td>On macOS, while fullscreen, pressing the escape key will not fire keyup</td>
    <td>Breaks logic which assumes that key events are reliable</td>
    <td><a href="">WebKit Bugzilla Ticket</a> (reported Todo)</td>
</tr>
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
<tr>
    <td>2023-06-11</td>
    <td><a href="2023-06-11-firefox-line-bug">View</a></td>
    <td>Visual glitches in canvas when drawing a line.</td>
    <td>Drawing applications will draw glitchy strokes on Windows.</td>
    <td><a href="https://bugzilla.mozilla.org/show_bug.cgi?id=1837870">Bugzilla Ticket</a> (reported 2023-06-11)</td>
</tr>
<tr>
    <td>2023-11-03</td>
    <td><a href="2023-11-03-firefox-canvas-alpha">View</a></td>
    <td>globalCompositeOperation makes canvas without alpha channel transparent</td>
    <td>Higher memory use, and slower rendering.</td>
    <td><a href="https://bugzilla.mozilla.org/show_bug.cgi?id=1862925">Bugzilla Ticket</a> (reported 2023-11-03)</td>
</tr>
<tr>
    <td>2024-09-02</td>
    <td><a href="2024-09-02-firefox-mac-escape-key">View</a></td>
    <td>On macOS, while fullscreen, pressing the escape key will not fire keyup</td>
    <td>Breaks logic which assumes that key events are reliable</td>
    <td><a href="https://bugzilla.mozilla.org/show_bug.cgi?id=1916279">Bugzilla Ticket</a> (reported 2024-09-02)</td>
</tr>
</table>


# Fixed (Archive)
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
    <td>2024-06-23</td>
    <td><a href="2024-06-23-chrome-small-arc">View</a></td>
    <td>Context2d arc() fill() draws strange shapes for small radii.</td>
    <td>Applications relying on the canvas arc method achieve bad quality circles. I.e. the pen tool in Kleki/Klecks looks much worse.</td>
    <td><a href="https://issues.chromium.org/issues/348683485">Chromium Ticket</a> (reported 2024-06-23, fixed 2024-07-24 in Chrome 127)</td>
</tr>
<tr>
    <td>2023-05-06</td>
    <td>kleki.com</td>
    <td>canvas.context('webgl') fails on Chrome OS on some pages (not on all devices)</td>
    <td>Features relying on WebGL do not work (filters in Kleki/Klecks)</td>
    <td><a href="https://bugs.chromium.org/p/chromium/issues/detail?id=1443160">Chromium Ticket</a> (reported 2023-05-06, fixed 2023-06-14)</td>
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
<tr>
    <td>2023-04-30</td>
    <td><a href="2023-04-30-safari-putimagedata">View</a></td>
    <td>Canvas putImageData draws onto wrong canvas.</td>
    <td>If you duplicate canvases, the putImageData method becomes unreliable. I.e. it breaks the paint bucket in Kleki/Klecks without a special workaround.</td>
    <td><a href="https://bugs.webkit.org/show_bug.cgi?id=256151">WebKit Bugzilla Ticket</a> (reported on 2023-04-30, fixed 2023-05-11)</td>
</tr>
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
</table>



# todo
- chrome invert artifacts https://github.com/bitbof/klecks/issues/8
- safari canvas gradient -> webgl glitch https://github.com/bitbof/klecks/issues/41
- firefox text repositioning after scrolling
- safari apple pencil pressure very high in first event?
- chrome after lifting stylus one pointerevent in position of pointerdown?



