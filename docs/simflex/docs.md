`simflex` is based on `real-12et`, but:

- Continuous mode removed.
- Instead of global ET system (12), each scale now can have their own ET systems.
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
