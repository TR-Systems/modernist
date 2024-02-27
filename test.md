## Style Sheet Test Page

#### Table Testing
Trying to fill a table data cell with a background color.

| Hex Code | Color |
| -------- | ----- |
| #6C7989 | <span style="font-size:36px;height:36px;width:36px;background:#6C7989;"> x </span> |
| next | next |

| Type | Model | Firmware | Web Version | Purchased |
| ---- | ----- | -------- | ----------- | --------- |
| Outdoor Mini-Dome (4) | DS-2CD-2543-G0-IS | v5.5.61 b180718<br>v5.6.820 b220519<br>v5.6.821 b230831 | v4.0.1 b180626<br>v4.0.1 b220610 | 3 in 2018<br>1 in 2023 |
| Indoor Cube w/PIR | DS-2CD-2422-FWD-IW | v5.5.0 b170725 | v4.0.1 b170711 | 2018  |
| Outdoor PTZ Mini-Dome | DS-2DE-3404-W-DE | v5.7.4 b221130<br>v5.8.1 b231108 | v4.0.1 b220121 | 2024 |
| NVR | DS-7604-NI-Q1 | v4.32.110 b211009 | v4.0.1 b210914 | 2024 |

---

#### Picture Testing
Style sheet creates the background and border. Control the size in markdown using the width setting.

Make it small using width=10% (of what you may ask?)

<img width="10%" src="assets/images/zion-np.jpg" alt="Bike">

Or big using width=320 (pixels)

<img width="320" src="assets/images/zion-np.jpg">

Placing text and other content next to an image can be done in several ways and gets really complicated really fast, but I got his working with some custom styling and some html in the page source.

This is a "grid" element with two columns. The style sheet sets the width of the first column to 40%, for a big picture. I'm still working on giving that more flexibility. Like I said, it's complicated.

<div class="image-grid">
<div class="item1">
    <img src="assets/images/zion-np.jpg">
</div>
<div class="item2">
<hr>
<p>Virgin River - Zion National Park</p>
<hr>
<p>Continue adding text to this grid element and it will flow alongside, remaining in this column and continuing past the bottom of the picture.</p>
<p>In the source markdown, you can add additional div sections to define additional grid elements in sequence using additional div statements.</p>
</div>
<div class="item3">
<p>Next element in the grid and the margin is wrong. I know why but it would take too long to explain.</p>
<p>There is one thing I'm doing that throws everything off and that's the 8px picture frame around all images, also too hard to explain.</p>
</div>
<div class="item4">
<p>Last element in the grid, with a picture after two breaks, otherwise the pic shifts left. More styling issues with margins and padding.<br><br>
<img width="100" src="assets/images/zion-np.jpg"><br>
More text after another break.</p>
</div>
</div>

---

#### Pipe Testing
Using the Pipe/Vertical Bar Symbol yields table cells

| One pipe, one table data cell

| Two pipes with image after the second.<br>Table styling in the style sheet modifies<br>image style to remove the picture frame<br>but retains the rounded radius border. | <img width="160" src="assets/images/zion-np.jpg">

Fun stuff...

---

End of Document
