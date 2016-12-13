# copy-event-attributes

This was pulled out of [yo-yo](https://github.com/maxogden/yo-yo) because I wanted the nicer [morphdom](https://github.com/patrick-steele-idem/morphdom) it provides, but without the dependency on [bel](https://github.com/shama/bel)

### install

###### yarn
```shell
yarn add copy-event-attributes
```

###### npm
```shell
npm install --save copy-event-attributes
```

### usage

```javascript
var copyEvents = require('copy-event-attributes')

copyEvents(fromEl, toEl)
```

### usage with morphdom

```javascript
var copyEvents = require('copy-event-attributes')
var morphdom = require('morphdom')

morphdom(fromEl, toEl, {
  onBeforeElUpdated: copyEvents
})
```

### usage with custom events


```javascript
var copyEvents = require('copy-event-attributes')
var morphdom = require('morphdom')

function copyCustomEvents (fromEl, toEl) {
  return copyEvents(fromEl, toEl, ['onmyevent'])
}

morphdom(fromEl, toEl, {
 onBeforeElUpdated: copyCustomEvents
})
```
