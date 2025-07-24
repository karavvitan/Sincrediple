> - SFMBE.

*The codes were created by ChatGPT. (I don't understand coding yet, esp. JavaScript.)*

This is an app for playing music based on scale presets. Good for fun playing, education, and for beginners.

Try them:

1. [Basic](https://karavvitan.github.io/Sincrediple/2025/05/10/basic.html)
2. [Advanced Audio Logic 12ET Notation](https://karavvitan.github.io/Sincrediple/2025/06/15/advancedaudio12et.html)
3. [Advanced Audio Logic Ratio Notation](https://karavvitan.github.io/Sincrediple/2025/06/15/advancedaudioratio.html)
4. ["Every octave in continuous mode is divided into two rows" version](https://karavvitan.github.io/Sincrediple/2025/07/18/stretched_continuous.html)

The codes are in the `_posts` folder.

## Featured

1. **XY dimensionality: X for pitch, Y for the volume**
2. **Multioctave**

They can be configured here:
```js
const numOctaves = 6; // number of octaves
const baseOctave = -1; // base octave, based on 'baseFreq'
```
3. **Scale options: configurable defined scales or linear continuous pad**

To add or configure scales, look at
```html
  <div id="scaleButtonContainer">
    <select id="scaleSelect">
```
(in `<body>` element) and
```js
const scalePresets = {
```
(in `<script>` element), and just understand the patterns. Every `[]` must be ended with a comma except the last.

Example:

```html
  <div id="scaleButtonContainer">
    <select id="scaleSelect">
      <option value="blues">Blues</option>
      <option value="tizitaminor">Tizita Minor</option>
      <option value="rast">Rast</option>
      <option value="iwato">Iwato</option>
      <option value="degung">Degung</option>
      <option value="continuous">Continuous</option>
    </select>
  </div>
```
in `body` element, and
```js
    const scalePresets = {
      blues: [0, 3, 5, 6, 7, 10],
      tizitaminor: [0, 2.04, 3.16, 7.02, 8.14],
      rast: [0, 2, 3.5, 5, 7, 9, 10.5],
      iwato: [0, 1, 5, 6, 10],
      degung: [0, 3.863, 4.98, 7.02, 10.883]
    };
```
in `script` element. (Sorry if I misrepresent them, the resources of world music scales in internet are very limited.)

4. **Automatic coloring and decimal 12ET/ratio notation labeling**

Tones are colored automatically based on their values.

6. **Adjustable rows height**

Need more space for X/volume controll? Just edit the value of `height:` in `.octave-row {}` in `<style>`**,** and `rowHeight =` in `<script>`.
> [!NOTE] Important!
> Ensure that the values of both are the same or the visual and the actual pad won't be aligned.

6. **Customizable audio generator**
Unfortunately I find it difficult to explain, so just figure out yourself.

## Notes
1. Sometimes the visual and the actual pad aren't aligned, try to refresh the page if this happens.
