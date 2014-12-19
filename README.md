# localforage-find

Adds find function to [localforage](http://mozilla.github.io/localForage/).

## Usage

```
var localforage = require('localforage');
require('localforage-find')(localforage);

// using promises
localforage.find(function(key, value) {
  return value.score > 20;
}).then(function(resultsArray) {

});

// using callbacks
localforage.find(function(key, value) {
  return value.score > 20;
}, function(err, resultsArray) {

});
```

Order of resultsArray is not guaranteed.

## Install

```
npm install localforage-find
```

## Run Tests

You may need to delete ~/.config/browser-launcher/ first.

```
npm test
```

## License

MIT