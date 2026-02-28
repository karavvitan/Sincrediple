> [!NOTE]
> - Sorry for my bad English.
> - The codes were created by ChatGPT. I don't understand coding yet, (especially when I first made this project).

This is a simple HTML app for playing music based on scale presets.
Good for fun playing, education, and for beginners.

Try them:

1. [Real 12-ET Notation Based (v0)](https://karavitan.github.io/Sincrediple/real-12et/)
2. [Ratio Notation Based (v0)](https://karavitan.github.io/Sincrediple/ratio/)
3. ["Every octave in continuous mode is divided into two rows" version (v1)](https://karavitan.github.io/Sincrediple/splitted-continuous/)

The source codes are in `/docs` folder (named so for easy deploying to gh-pages).

## Featured

1. **XY dimensionality: X for the pitch, Y for the volume**
2. **Multioctave**

They can be configured here:

```js
const numOctaves = 6; // number of octaves
const baseOctave = -1; // base octave, based on 'baseFreq'
```

3. **Scale options: configurable defined scales or perceptionally linear continuous pad**

(This explanation is mainly for **v0**—**v1**)  
To add or configure scales, look at

```html
  <div id="scaleButtonContainer">
    <select id="scaleSelect">
```

(in `<body>` element) and

```js
const scalePresets = {
```

(in `<script>` element), and just understand the pattern. Every `[]` must be ended with a comma except the last.

Example:

```html
  <div id="scaleButtonContainer">
    <select id="scaleSelect">
      <option value="pelog">Pelog</option>
      <option value="sorog">Sorog</option>
      <option value="rast">Rast</option>
    </select>
  </div>
```

in `body` element, and

```js
    const scalePresets = {
      pelog: [0, 0.96, 2.86, 6.88, 7.82], // 'Music in Java', Kunst, p. 395
      sorog: [0, 0.96, 4.98, 7.08, 8.02], // ibid
      rast: [0, 2.04, 3.55, 4.98, 7.02, 8.58, 9.97], // tuning.abletone.com
    };
```

in `script` element.

4. **Automatic coloring and real ET/ratio notation labeling**

Tones are colored automatically based on their values.

6. **Adjustable rows height**

Need more space for X/volume controll?
Just edit the value of `height:` in `.octave-row {}` in `<style>`**,** and `rowHeight =` in `<script>`.

> [!WARNING]
> Ensure that the values of both are the same or the visual and the actual pad won't be aligned.

6. **Customizable audio generator**

Unfortunately I'm too lazy to explain, so just figure out yourself.

## Notes

1. Sometimes the visual and the actual pad aren't aligned, try to refresh the page if this happens.
