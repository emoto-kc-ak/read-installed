# read-installed

Read all the installed packages in a folder, and return a tree
structure with all the data.

npm uses this.

## 2.0.0

Breaking changes in `2.0.0`:

The second argument is now an `Object` that contains the following keys:

 * `depth` optional, defaults to Infinity
 * `log` optional log Function
 * `dev` optional, default false, set to true to include devDependencies
 * `tree` optional, default false, set to true to build a tree precisely representing direct relationships among package.json files. no extraneous packages are outputted

## Usage

```javascript
var readInstalled = require("read-installed")
// optional options
var options = { dev: false, tree: false, log: fn, depth: 2 }
readInstalled(folder, options, function (er, data) {
  ...
})
```
