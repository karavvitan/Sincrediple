`simflex` is based on `real-12et`, but:

- **Continuous mode removed (more `sim`ple).**

  The reason is, the sliding sounds unnatural,
  it really differs from sliding with acoustic instruments.
  I don't really know the reason and i'm still far from understanding this stuff.
  So I just think the mode would be useless.

- **Instead of global ET system (12), each scale now can have their own ET systems (more `flex`ible).**

  So, the `scalePresets` properties format now is:

  ```
  scaleName: [ETSystem, scaleArray]
  ```

  For example:

  ```
  const scalePresets = {
  …
  minor: [1200, [0, 200, 300, 500, 700, 800, 1000]],
  …
  ```

- **At the same code, you can also use ratio notation for scales (more `flex`ible).**

  To use it, set `ETSystem` to `0`.

  For example:

  ```
  minor: [0, [1/1, 9/8, 6/5, 4/3, 3/2, 8/5, 9/5]]
  ```
