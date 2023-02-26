<h1 align="center">Welcome to dye.js 👋</h1>
<p>
  <img alt="Version" src="https://img.shields.io/badge/version-0.4-blue.svg?cacheSeconds=2592000" />
  <img src="https://img.shields.io/badge/npm-%3E%3D8.19.2-blue.svg" />
  <img src="https://img.shields.io/badge/node-%3E%3D16.17.0-blue.svg" />
  <a href="https://github.com/Slaveworx/dye.js#readme" target="_blank">
    <img alt="Documentation" src="https://img.shields.io/badge/documentation-yes-brightgreen.svg" />
  </a>
  <a href="https://github.com/Slaveworx/dye.js/graphs/commit-activity" target="_blank">
    <img alt="Maintenance" src="https://img.shields.io/badge/Maintained%3F-yes-green.svg" />
  </a>
  <a href="https://github.com/Slaveworx/dye.js/stable/LICENSE" target="_blank">
    <img alt="License: MIT" src="https://img.shields.io/github/license/Slaveworx/dye.js/stable/" />
  </a>
</p>

> Tiny and Blazing Fast Library that changes HTML elements' colors based on their self or parent background color.

### 🏠 [Homepage](https://deviago.me)

## Prerequisites

- npm >=8.19.2
- node >=16.17.0
- Works in any modern browser

## Usage

### ELEMENTS

Just apply the property "dye" to any regular HTML element and see the magic happen.
Please note that the `dye` attribute by itself _will only work with elements that have a background color themselves_.

```html
<p dye>This element will change color depending on self background color</p>
```

The instruction above will only work on element which have a background color themselves or in images in which the parent element has a background color.

If that is not the case, then you need to specify the parent:

```html
<p dye=".this-is-the-element-with-bg">
  This element will change color depending on the provided element's background
  color
</p>
```

### IMAGES

At the moment, this library only changes the color of black / white images or icons.

So you just follow the same logic as above, but there is a small catch: if your source image is originally black, you need to specify another parameter (`blackimg`) to the element:

```html
<img src="blackimage.png" dye="#this-is-an-id" blackimg>This element will change color depending on the parent background color</img>
```

Note: by default, when the element is an image, the library will always check the parent background color. If you wish to use another color in a remote relative, just provide the element to the `dye=""` parameter.

```html
<img src="blackimage.png" dye="#this-in-the-element-with-bg-color" blackimg>This element will change color depending on the parent background color</img>
```

### Gradients

From version 0.4.3 dye.js now supports gradients up to three colors.

Please bear in mind that depending on gradient direction or gradient transparencies and color positions, the output might not be 100% accurate.
However, dye.js works very well with relatively simple gradient backgrounds.
Note: this feature only works changing text color for now.
Note 2: This feature supports colors in RGB, RGBA, and HEX.

To use it you just need to add the `gradient` attribute to elements that have a gradient background and that you wish to change color dynamically.

```html
<p dye="#this-in-the-parent-id-with-gradient-bg" gradient>
  This element will change color depending on the parent gradient background.
</p>
```

### IMPORTANT NOTES

When you specify a selector, you need to identify it as a `class` or `id`, so please use the below syntax:

```html
<img src="blackimage.png" dye="#this-is-an-id" blackimg>This element will change color depending on the parent background color</img>
```

```html
<img src="blackimage.png" dye=".this-is-an-class" blackimg>This element will change color depending on the parent background color</img>
```

Note that we use `.` or `#` to let dye.js know that the selector is and `id` or `class`.

## Author

👤 **Tiago M. Galvão**

- Website: http://deviago.me
- Github: [@Slaveworx](https://github.com/Slaveworx)

## 🤝 Contributing

Contributions, issues and feature requests are welcome!<br />Feel free to check [issues page](https://github.com/Slaveworx/dye.js/issues).

## Show your support

Give a ⭐️ if this project helped you!

## 📝 License

Copyright © 2023 [Tiago M. Galvão](https://github.com/Slaveworx).<br />
This project is [MIT](https://github.com/Slaveworx/dye.js/blob/master/LICENSE) licensed.

---
