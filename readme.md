#entities [![NPM version](http://img.shields.io/npm/v/entities.svg)](https://npmjs.org/package/entities)  [![Downloads](https://img.shields.io/npm/dm/entities.svg)](https://npmjs.org/package/entities) [![Build Status](http://img.shields.io/travis/fb55/entities.svg)](http://travis-ci.org/fb55/entities) [![Coverage](http://img.shields.io/coveralls/fb55/entities.svg)](https://coveralls.io/r/fb55/entities)

En- & decoder for XML/HTML entities.  Uses some non-standard character mapping to better support sending text messages in the GSM format.

##How to…

###…install `entities`

    npm i entities

###…use `entities`

```javascript
var entities = require("entities");
//encoding
entities.encodeXML("&#38;");  // "&amp;#38;"
entities.encodeHTML("&#38;"); // "&amp;&num;38&semi;"
//decoding
entities.decodeXML("asdf &amp; &#xFF; &#xFC; &apos;");  // "asdf & ÿ ü '"
entities.decodeHTML("asdf &amp; &yuml; &uuml; &apos;"); // "asdf & ÿ ü '"
```

<!-- TODO extend API -->

---

License: BSD-like
