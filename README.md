# api documentation for  [html-to-text (v3.2.0)](https://github.com/werk85/node-html-to-text)  [![npm package](https://img.shields.io/npm/v/npmdoc-html-to-text.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-html-to-text) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-html-to-text.svg)](https://travis-ci.org/npmdoc/node-npmdoc-html-to-text)
#### Advanced html to plain text converter

[![NPM](https://nodei.co/npm/html-to-text.png?downloads=true)](https://www.npmjs.com/package/html-to-text)

[![apidoc](https://npmdoc.github.io/node-npmdoc-html-to-text/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-html-to-text_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-html-to-text/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-html-to-text/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-html-to-text/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Malte Legenhausen",
        "email": "legenhausen@werk85.de"
    },
    "bin": {
        "html-to-text": "./bin/cli.js"
    },
    "bugs": {
        "url": "https://github.com/werk85/node-html-to-text/issues"
    },
    "dependencies": {
        "he": "^1.0.0",
        "htmlparser2": "^3.9.2",
        "optimist": "^0.6.1",
        "underscore": "^1.8.3",
        "underscore.string": "^3.2.3"
    },
    "description": "Advanced html to plain text converter",
    "devDependencies": {
        "chai": "^3.5.0",
        "eslint": "^3.14.1",
        "istanbul": "^0.4.5",
        "mocha": "^3.0.0"
    },
    "directories": {},
    "dist": {
        "shasum": "0dfa5d27ff816b07281c79eaf60d408744ac6d89",
        "tarball": "https://registry.npmjs.org/html-to-text/-/html-to-text-3.2.0.tgz"
    },
    "engines": {
        "node": ">= 0.10.0"
    },
    "gitHead": "8782c3d4d6d2f41b276ce5562cb3d5f39fdd0079",
    "homepage": "https://github.com/werk85/node-html-to-text",
    "keywords": [
        "html",
        "node",
        "text",
        "mail",
        "plain",
        "converter"
    ],
    "license": "MIT",
    "main": "index.js",
    "maintainers": [
        {
            "name": "mlegenhausen",
            "email": "mlegenhausen@gmail.com"
        }
    ],
    "name": "html-to-text",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/werk85/node-html-to-text.git"
    },
    "scripts": {
        "example": "node ./example/html-to-text.js",
        "lint": "eslint .",
        "test": "istanbul cover _mocha && eslint ."
    },
    "version": "3.2.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module html-to-text](#apidoc.module.html-to-text)
1.  [function <span class="apidocSignatureSpan">html-to-text.</span>fromFile (file, options, callback)](#apidoc.element.html-to-text.fromFile)
1.  [function <span class="apidocSignatureSpan">html-to-text.</span>fromString (str, options)](#apidoc.element.html-to-text.fromString)
1.  object <span class="apidocSignatureSpan">html-to-text.</span>formatter
1.  object <span class="apidocSignatureSpan">html-to-text.</span>helper

#### [module html-to-text.formatter](#apidoc.module.html-to-text.formatter)
1.  [function <span class="apidocSignatureSpan">html-to-text.formatter.</span>anchor (elem, fn, options)](#apidoc.element.html-to-text.formatter.anchor)
1.  [function <span class="apidocSignatureSpan">html-to-text.formatter.</span>heading (elem, fn, options)](#apidoc.element.html-to-text.formatter.heading)
1.  [function <span class="apidocSignatureSpan">html-to-text.formatter.</span>horizontalLine (elem, fn, options)](#apidoc.element.html-to-text.formatter.horizontalLine)
1.  [function <span class="apidocSignatureSpan">html-to-text.formatter.</span>image (elem, options)](#apidoc.element.html-to-text.formatter.image)
1.  [function <span class="apidocSignatureSpan">html-to-text.formatter.</span>lineBreak (elem, fn, options)](#apidoc.element.html-to-text.formatter.lineBreak)
1.  [function <span class="apidocSignatureSpan">html-to-text.formatter.</span>listItem (prefix, elem, fn, options)](#apidoc.element.html-to-text.formatter.listItem)
1.  [function <span class="apidocSignatureSpan">html-to-text.formatter.</span>orderedList (elem, fn, options)](#apidoc.element.html-to-text.formatter.orderedList)
1.  [function <span class="apidocSignatureSpan">html-to-text.formatter.</span>paragraph (elem, fn, options)](#apidoc.element.html-to-text.formatter.paragraph)
1.  [function <span class="apidocSignatureSpan">html-to-text.formatter.</span>table (elem, fn, options)](#apidoc.element.html-to-text.formatter.table)
1.  [function <span class="apidocSignatureSpan">html-to-text.formatter.</span>text (elem, options)](#apidoc.element.html-to-text.formatter.text)
1.  [function <span class="apidocSignatureSpan">html-to-text.formatter.</span>unorderedList (elem, fn, options)](#apidoc.element.html-to-text.formatter.unorderedList)

#### [module html-to-text.helper](#apidoc.module.html-to-text.helper)
1.  [function <span class="apidocSignatureSpan">html-to-text.helper.</span>arrayZip (array)](#apidoc.element.html-to-text.helper.arrayZip)
1.  [function <span class="apidocSignatureSpan">html-to-text.helper.</span>splitCssSearchTag (tagString)](#apidoc.element.html-to-text.helper.splitCssSearchTag)
1.  [function <span class="apidocSignatureSpan">html-to-text.helper.</span>wordwrap (text, options)](#apidoc.element.html-to-text.helper.wordwrap)



# <a name="apidoc.module.html-to-text"></a>[module html-to-text](#apidoc.module.html-to-text)

#### <a name="apidoc.element.html-to-text.fromFile"></a>[function <span class="apidocSignatureSpan">html-to-text.</span>fromFile (file, options, callback)](#apidoc.element.html-to-text.fromFile)
- description and source-code
```javascript
fromFile = function (file, options, callback) {
  if (!callback) {
    callback = options;
    options = {};
  }
  fs.readFile(file, 'utf8', function (err, str) {
    if (err) return callback(err);
    return callback(null, htmlToText(str, options));
  });
}
```
- example usage
```shell
...

## Usage
You can read from a file via:

'''javascript
var htmlToText = require('html-to-text');

htmlToText.fromFile(path.join(__dirname, 'test.html'), {
	tables: ['#invoice', '.address']
}, (err, text) => {
	if (err) return console.error(err);
	console.log(text);
});
'''
...
```

#### <a name="apidoc.element.html-to-text.fromString"></a>[function <span class="apidocSignatureSpan">html-to-text.</span>fromString (str, options)](#apidoc.element.html-to-text.fromString)
- description and source-code
```javascript
fromString = function (str, options) {
  return htmlToText(str, options || {});
}
```
- example usage
```shell
...
'''

or directly from a string:

'''javascript
var htmlToText = require('html-to-text');

var text = htmlToText.fromString('<h1>Hello World</h1>', {
	wordwrap: 130
});
console.log(text);
'''

### Options:
...
```



# <a name="apidoc.module.html-to-text.formatter"></a>[module html-to-text.formatter](#apidoc.module.html-to-text.formatter)

#### <a name="apidoc.element.html-to-text.formatter.anchor"></a>[function <span class="apidocSignatureSpan">html-to-text.formatter.</span>anchor (elem, fn, options)](#apidoc.element.html-to-text.formatter.anchor)
- description and source-code
```javascript
function formatAnchor(elem, fn, options) {
  var href = '';
  // Always get the anchor text
  var storedCharCount = options.lineCharCount;
  var text = fn(elem.children || [], options);
  if (!text) {
    text = '';
  }

  var result = elem.trimLeadingSpace ? _s.lstrip(text) : text;

  if (!options.ignoreHref) {
    // Get the href, if present
    if (elem.attribs && elem.attribs.href) {
      href = elem.attribs.href.replace(/^mailto\:/, '');
    }
    if (href) {
      if (options.linkHrefBaseUrl && href.indexOf('/') === 0) {
        href = options.linkHrefBaseUrl + href;
      }
      if (!options.hideLinkHrefIfSameAsText || href !== _s.replaceAll(result, '\n', '')) {
        if (!options.noLinkBrackets) {
          result += ' [' + href + ']';
        } else {
          result += ' ' + href;
        }
      }
    }
  }

  options.lineCharCount = storedCharCount;

  return formatText({ data: result || href, trimLeadingSpace: elem.trimLeadingSpace }, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.html-to-text.formatter.heading"></a>[function <span class="apidocSignatureSpan">html-to-text.formatter.</span>heading (elem, fn, options)](#apidoc.element.html-to-text.formatter.heading)
- description and source-code
```javascript
function formatHeading(elem, fn, options) {
  var heading = fn(elem.children, options);
  if (options.uppercaseHeadings) {
    heading = heading.toUpperCase();
  }
  return heading + '\n';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.html-to-text.formatter.horizontalLine"></a>[function <span class="apidocSignatureSpan">html-to-text.formatter.</span>horizontalLine (elem, fn, options)](#apidoc.element.html-to-text.formatter.horizontalLine)
- description and source-code
```javascript
function formatHorizontalLine(elem, fn, options) {
  return '\n' + _s.repeat('-', options.wordwrap) + '\n\n';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.html-to-text.formatter.image"></a>[function <span class="apidocSignatureSpan">html-to-text.formatter.</span>image (elem, options)](#apidoc.element.html-to-text.formatter.image)
- description and source-code
```javascript
function formatImage(elem, options) {
  if (options.ignoreImage) {
    return '';
  }

  var result = '', attribs = elem.attribs || {};
  if (attribs.alt) {
    result += he.decode(attribs.alt, options.decodeOptions);
    if (attribs.src) {
      result += ' ';
    }
  }
  if (attribs.src) {
    result += '[' + attribs.src + ']';
  }
  return (result);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.html-to-text.formatter.lineBreak"></a>[function <span class="apidocSignatureSpan">html-to-text.formatter.</span>lineBreak (elem, fn, options)](#apidoc.element.html-to-text.formatter.lineBreak)
- description and source-code
```javascript
function formatLineBreak(elem, fn, options) {
  return '\n' + fn(elem.children, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.html-to-text.formatter.listItem"></a>[function <span class="apidocSignatureSpan">html-to-text.formatter.</span>listItem (prefix, elem, fn, options)](#apidoc.element.html-to-text.formatter.listItem)
- description and source-code
```javascript
function formatListItem(prefix, elem, fn, options) {
  options = _.clone(options);
  // Reduce the wordwrap for sub elements.
  if (options.wordwrap) {
    options.wordwrap -= prefix.length;
  }
  // Process sub elements.
  var text = fn(elem.children, options);
  // Replace all line breaks with line break + prefix spacing.
  text = text.replace(/\n/g, '\n' + _s.repeat(' ', prefix.length));
  // Add first prefix and line break at the end.
  return prefix + text + '\n';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.html-to-text.formatter.orderedList"></a>[function <span class="apidocSignatureSpan">html-to-text.formatter.</span>orderedList (elem, fn, options)](#apidoc.element.html-to-text.formatter.orderedList)
- description and source-code
```javascript
function formatOrderedList(elem, fn, options) {
  var result = '';
  var nonWhiteSpaceChildren = (elem.children || []).filter(function(child) {
    return child.type !== 'text' || !whiteSpaceRegex.test(child.data);
  });
  // Return different functions for different OL types
  var typeFunctions = {
    1: function(start, i) { return i + 1 + start},
    a: function(start, i) { return String.fromCharCode(i + start + 97)},
    A: function(start, i) { return String.fromCharCode(i + start + 65)}
  };
  // Determine type
  var olType = elem.attribs.type || '1'
  // Make sure there are list items present
  if (nonWhiteSpaceChildren.length) {
    // Calculate initial start from ol attribute
    var start = Number(elem.attribs.start || '1') - 1
    // Calculate the maximum length to i.
    var maxLength = (nonWhiteSpaceChildren.length + start).toString().length;
    _.each(nonWhiteSpaceChildren, function(elem, i) {
      // Use different function depending on type
      var index = typeFunctions[olType](start, i);
      // Calculate the needed spacing for nice indentation.
      var spacing = maxLength - index.toString().length;
      var prefix = (olType === '1') ? ' ' + index + '. ' + _s.repeat(' ', spacing) : index + '. ';
      result += formatListItem(prefix, elem, fn, options);
    });
  }
  return result + '\n';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.html-to-text.formatter.paragraph"></a>[function <span class="apidocSignatureSpan">html-to-text.formatter.</span>paragraph (elem, fn, options)](#apidoc.element.html-to-text.formatter.paragraph)
- description and source-code
```javascript
function formatParagraph(elem, fn, options) {
  var paragraph = fn(elem.children, options)
  if (options.singleNewLineParagraphs) {
    return paragraph + '\n'
  } else {
    return paragraph + '\n\n'
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.html-to-text.formatter.table"></a>[function <span class="apidocSignatureSpan">html-to-text.formatter.</span>table (elem, fn, options)](#apidoc.element.html-to-text.formatter.table)
- description and source-code
```javascript
function formatTable(elem, fn, options) {
  var table = [];
  _.each(elem.children, tryParseRows);
  return tableToString(table);

  function tryParseRows(elem) {
    if (elem.type !== 'tag') {
      return;
    }
    switch (elem.name.toLowerCase()) {
      case "thead":
      case "tbody":
      case "tfoot":
      case "center":
        _.each(elem.children, tryParseRows);
        return;

      case 'tr':
        var rows = [];
        _.each(elem.children, function(elem) {
          var tokens, times;
          if (elem.type === 'tag') {
            switch (elem.name.toLowerCase()) {
              case 'th':
                tokens = formatHeading(elem, fn, options).split('\n');
                rows.push(_.compact(tokens));
                break;

              case 'td':
                tokens = fn(elem.children, options).split('\n');
                rows.push(_.compact(tokens));
                // Fill colspans with empty values
                if (elem.attribs && elem.attribs.colspan) {
                  times = elem.attribs.colspan - 1 || 0;
                  _.times(times, function() {
                    rows.push(['']);
                  });
                }
                break;
            }
          }
        });
        rows = helper.arrayZip(rows);
        _.each(rows, function(row) {
          row = _.map(row, function(col) {
            return col || '';
          });
          table.push(row);
        });
        break;
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.html-to-text.formatter.text"></a>[function <span class="apidocSignatureSpan">html-to-text.formatter.</span>text (elem, options)](#apidoc.element.html-to-text.formatter.text)
- description and source-code
```javascript
function formatText(elem, options) {
  var text = elem.data || "";
  text = he.decode(text, options.decodeOptions);

  if (options.isInPre) {
    return text;
  } else {
    return helper.wordwrap(elem.trimLeadingSpace ? _s.lstrip(text) : text, options);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.html-to-text.formatter.unorderedList"></a>[function <span class="apidocSignatureSpan">html-to-text.formatter.</span>unorderedList (elem, fn, options)](#apidoc.element.html-to-text.formatter.unorderedList)
- description and source-code
```javascript
function formatUnorderedList(elem, fn, options) {
  var result = '';
  var nonWhiteSpaceChildren = (elem.children || []).filter(function(child) {
    return child.type !== 'text' || !whiteSpaceRegex.test(child.data);
  });
  _.each(nonWhiteSpaceChildren, function(elem) {
    result += formatListItem(' * ', elem, fn, options);
  });
  return result + '\n';
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.html-to-text.helper"></a>[module html-to-text.helper](#apidoc.module.html-to-text.helper)

#### <a name="apidoc.element.html-to-text.helper.arrayZip"></a>[function <span class="apidocSignatureSpan">html-to-text.helper.</span>arrayZip (array)](#apidoc.element.html-to-text.helper.arrayZip)
- description and source-code
```javascript
function arrayZip(array) {
  return _.zip.apply(_, array);
}
```
- example usage
```shell
...
// Convert all rows to lengths
var widths = _.map(table, function(row) {
  return _.map(row, function(col) {
    return col.length;
  });
});
// Invert rows with colums
widths = helper.arrayZip(widths);
// Determine the max values for each column
widths = _.map(widths, function(col) {
  return _.max(col);
});

// Build the table
var text = '';
...
```

#### <a name="apidoc.element.html-to-text.helper.splitCssSearchTag"></a>[function <span class="apidocSignatureSpan">html-to-text.helper.</span>splitCssSearchTag (tagString)](#apidoc.element.html-to-text.helper.splitCssSearchTag)
- description and source-code
```javascript
function splitCssSearchTag(tagString) {
  function getParams(re, string) {
    var captures = [], found;
    while ((found = re.exec(string)) !== null) {
      captures.push(found[1]);
    }
    return captures;
  }

  var splitTag = {};
  var elementRe = /(^\w*)/g;
  splitTag.element = elementRe.exec(tagString)[1];
  splitTag.classes = getParams( /\.([\d\w-]*)/g, tagString);
  splitTag.ids = getParams( /#([\d\w-]*)/g, tagString);

  return splitTag;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.html-to-text.helper.wordwrap"></a>[function <span class="apidocSignatureSpan">html-to-text.helper.</span>wordwrap (text, options)](#apidoc.element.html-to-text.helper.wordwrap)
- description and source-code
```javascript
function wordwrap(text, options) {
  var max = options.wordwrap;
  var preserveNewlines = options.preserveNewlines;
  var length = options.lineCharCount;

  // Preserve leading space
  var result = _s.startsWith(text, ' ') ? ' ' : '';
  length += result.length;
  var buffer = [];
  // Split the text into words, decide to preserve new lines or not.
  var words = preserveNewlines
    ? text.replace(/\n/g, '\n ').split(/\ +/)
    : _s.words(text);

  // Determine where to end line word by word.
  _.each(words, function(word) {
    // Add buffer to result if we can't fit any more words in the buffer.
    if ((max || max === 0) && length > 0 && ((length + word.length > max) || (length + word.indexOf('\n') > max))) {
      // Concat buffer and add it to the result
      result += buffer.join(' ') + '\n';
      // Reset buffer and length
      buffer.length = length = 0;
    }

    // Check if the current word is long enough to be wrapped
    if ((max || max === 0) && (options.longWordSplit) && (word.length > max)) {
      word = splitLongWord(word, options);
    }

    buffer.push(word);

    // If the word contains a newline then restart the count and add the buffer to the result
    if (word.indexOf('\n') !== -1) {
      result += buffer.join(' ');

      // Reset the buffer, let the length include any characters after the last newline
      buffer.length = 0;
      length = word.length - (word.lastIndexOf('\n') + 1);
      // If there are characters after the newline, add a space and increase the length by 1
      if (length) {
        result += ' ';
        length++;
      }
    } else {
      // Add word length + one whitespace
      length += word.length + 1;
    }
  });
  // Add the rest to the result.
  result += buffer.join(' ');

  // Preserve trailing space
  if (!_s.endsWith(text, ' ')) {
    result = _s.rtrim(result);
  } else if (!_s.endsWith(result, ' ')) {
    result = result + ' ';
  }

  return result;
}
```
- example usage
```shell
...
function formatText(elem, options) {
var text = elem.data || "";
text = he.decode(text, options.decodeOptions);

if (options.isInPre) {
  return text;
} else {
  return helper.wordwrap(elem.trimLeadingSpace ? _s.lstrip(text) : text, options);
}
}

function formatImage(elem, options) {
if (options.ignoreImage) {
  return '';
}
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
