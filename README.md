# cache param file loader for webpack

## Usage

[Documentation: Using loaders](http://webpack.github.io/docs/using-loaders.html)

The `cache param file` loader works like the `file` loader, but adds a cache invalidation parameter to the path string it returns.

This can be used for css files where you'd want the browser to load the new resource, for example a webfont, that is specified in the css-file.

The cache parameter depends om the size of the file, so it should change if the file content has changed.


``` javascript
require("url?limit=10000!./file.png");
// => returns "/public-path/file.png?vXXXX" where vXXXX depends on the size of the file
```

For additional parameters and usage instructions see: [`file-loader`](https://github.com/webpack/file-loader).

## License

MIT (http://www.opensource.org/licenses/mit-license.php)