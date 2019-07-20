#d3-svg-to-png

Converts SVG elements in the browser to PNG and other image formats, while keeping CSS styles. Optionally, it returns the data as a promise or downloads it. It can also rescale the svg image, ignore certain DOM elements...

## Installation

```shell
$ npm i d3-svg-to-png
```

## Usage

```js
const d3ToPng = require('d3-svg-to-png');
d3ToPng('selector', 'name');
```

## Mandatory fields

- **Selector** (String): Commonly 'svg';
- **Name** (String): Name for the file output, without extension.

Output: **name.png**

## Options

```js
const d3ToPng = require('d3-svg-to-png');
d3ToPng('svg', 'name', { scale: 3, format: 'webp', quality: 0.01, download: false, ignore: '.ignored' }).then(fileData => {
  //do something with the data
});
```

- **scale** (number): Rescale the image by this factor. Default: _1_
- **format** (string): The format to output to. Compatibility might vary between browsers. See [HTMLCanvasElement.toDataURL()
  ](https://developer.mozilla.org/en-US/docs/Web/API/HTMLCanvasElement/toDataURL). Default: _png_
- **quality** (number): Between 0 (lowest) and 1. Affects formats with compression, like jpg. Default: _.92_
- **download** (boolean): Wether to download the resulting image. Default: _true_
- **ignore** (string): A CSS selector that, the matched elements of which will not me added to the output. Default: _null_

## Notes

Please report any problem, as this has not been thoroughly tested and could be improved.

## TODO

- Test on multiple browsers

## More creative coding

If you liked this you might like other [creative coding projects](https://tailorandwayne.com/coding-projects/).