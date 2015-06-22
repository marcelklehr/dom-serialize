dom-serialize
=============
### Serializes any DOM node into a String

It's like `outerHTML`, but it works with:

 * DOM elements
 * Text nodes
 * Attributes
 * Comment nodes
 * Documents
 * DocumentFragments
 * Doctypes
 * NodeLists / Arrays

Installation
------------

``` bash
$ npm install dom-serialize
```


Example
-------

``` js
var serialize = require('dom-serialize');
var node;

// works with Text nodes
node = document.createTextNode('foo & <bar>');
console.log(serialize(node));


// works with DOM elements
node = document.createElement('body');
node.appendChild(document.createElement('strong'));
node.firstChild.appendChild(document.createTextNode('hello'));
console.log(serialize(node));

```

```
foo &amp; &lt;bar&gt;
<body><strong>hello</strong></body>
```
