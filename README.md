# @jumpn/utils-array

> Array utilities (immutability, fp helpers)
>
> **NOTE**: All the functions described in [API](#API) are curried

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
<!-- END doctoc -->

- [Installation](#installation)
  - [Using npm](#using-npm)
  - [Using yarn](#using-yarn)
- [API](#api)
  - [append](#append)
  - [convertIfNot](#convertifnot)
  - [cycleNext](#cyclenext)
  - [fromObject](#fromobject)
  - [insert](#insert)
  - [isKey](#iskey)
  - [isLastIndex](#islastindex)
  - [isPossibleFromObject](#ispossiblefromobject)
  - [prepend](#prepend)
  - [reduceIf](#reduceif)
  - [reduceWhile](#reducewhile)
  - [remove](#remove)
  - [repeat](#repeat)
  - [replace](#replace)
  - [resolveIndex](#resolveindex)
- [License](#license)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## Installation

### Using [npm](https://docs.npmjs.com/cli/npm)

    $ npm install --save @jumpn/utils-array

### Using [yarn](https://yarnpkg.com)

    $ yarn add @jumpn/utils-array

## API

<!-- Generated by documentation.js. Update this documentation by updating the source code. -->

### append

Returns a new Array with elements appended to the one given.

**Parameters**

-   `elements` **[Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)&lt;[Element](https://developer.mozilla.org/en-US/docs/Web/API/Element)>** 
-   `array` **[Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)&lt;[Element](https://developer.mozilla.org/en-US/docs/Web/API/Element)>** 

Returns **[Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)&lt;[Element](https://developer.mozilla.org/en-US/docs/Web/API/Element)>** 

### convertIfNot

Returns input if it is an Array or returns a new Array with input inside if
it is not.

**Parameters**

-   `input` **Input** 

Returns **(Input | [Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)&lt;Input>)** 

### cycleNext

Returns 0 if current index is the last one, or returns next if it is not.

**Parameters**

-   `array` **[Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)&lt;any>** 
-   `currentIndex` **[number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)** 

Returns **[number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)** 

### fromObject

Creates a new array using the given object
If all of its entries are array keys.

(it could also have a property length with its size)

**Parameters**

-   `object` **[Object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)** 

Returns **[Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)&lt;any>** 

### insert

Returns a new Array with the result of having inserted the given elements at
the specified index.

**Parameters**

-   `index` **[number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)** 
-   `elements` **[Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)&lt;[Element](https://developer.mozilla.org/en-US/docs/Web/API/Element)>** 
-   `array` **[Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)&lt;[Element](https://developer.mozilla.org/en-US/docs/Web/API/Element)>** 

Returns **[Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)&lt;[Element](https://developer.mozilla.org/en-US/docs/Web/API/Element)>** 

### isKey

Returns true if the given string is an Array key or false otherwise.

**Parameters**

-   `string` **[string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)** 

Returns **[boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean)** 

### isLastIndex

Returns true if given index is the last one or false otherwise.

**Parameters**

-   `array` **[Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)&lt;any>** 
-   `index` **[number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)** 

Returns **[boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean)** 

### isPossibleFromObject

Returns true if an Array can be created from the given Object, or in other
words, if it has or not a length property, and the rest of its keys are Array
ones.

**Parameters**

-   `$0` **any** 
    -   `$0.length`  
    -   `$0.rest` **...any** 

Returns **[boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean)** 

### prepend

Returns a new Array with elements prepended to the one given.

**Parameters**

-   `elements` **[Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)&lt;[Element](https://developer.mozilla.org/en-US/docs/Web/API/Element)>** 
-   `array` **[Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)&lt;[Element](https://developer.mozilla.org/en-US/docs/Web/API/Element)>** 

Returns **[Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)&lt;[Element](https://developer.mozilla.org/en-US/docs/Web/API/Element)>** 

### reduceIf

Reduce the given array applying reduce function only to elements filtered.

**Parameters**

-   `filter` **Filter&lt;[Element](https://developer.mozilla.org/en-US/docs/Web/API/Element), Result>** 
-   `reduce` **Reduce&lt;[Element](https://developer.mozilla.org/en-US/docs/Web/API/Element), Result>** 
-   `resultInitial` **$Subtype&lt;Result>** 
-   `array` **[Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)&lt;$Subtype&lt;[Element](https://developer.mozilla.org/en-US/docs/Web/API/Element)>>** 

Returns **Result** 

### reduceWhile

Reduce the given array applying reduce function while shouldProceed function
returns true.

**Parameters**

-   `shouldProceed` **ShouldProceed&lt;[Element](https://developer.mozilla.org/en-US/docs/Web/API/Element), Result>** 
-   `reduce` **Reduce&lt;[Element](https://developer.mozilla.org/en-US/docs/Web/API/Element), Result>** 
-   `resultInitial` **Result** 
-   `array` **[Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)&lt;[Element](https://developer.mozilla.org/en-US/docs/Web/API/Element)>** 

Returns **Result** 

### remove

Returns a new Array with the result of having removed the specified amount
(count) of elements at the given index.

**Parameters**

-   `index` **[number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)** 
-   `count` **[number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)** 
-   `array` **[Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)&lt;[Element](https://developer.mozilla.org/en-US/docs/Web/API/Element)>** 

Returns **[Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)&lt;[Element](https://developer.mozilla.org/en-US/docs/Web/API/Element)>** 

### repeat

Returns a new Array with the given size (count) filled with the specified
element.

**Parameters**

-   `count` **[number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)** 
-   `element` **[Element](https://developer.mozilla.org/en-US/docs/Web/API/Element)** 

Returns **[Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)&lt;[Element](https://developer.mozilla.org/en-US/docs/Web/API/Element)>** 

### replace

Returns a new Array with the result of having replaced the elements at the
given index with the ones specified.

**Parameters**

-   `index` **[number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)** 
-   `elements` **[Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)&lt;[Element](https://developer.mozilla.org/en-US/docs/Web/API/Element)>** 
-   `array` **[Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)&lt;[Element](https://developer.mozilla.org/en-US/docs/Web/API/Element)>** 

Returns **[Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)&lt;[Element](https://developer.mozilla.org/en-US/docs/Web/API/Element)>** 

### resolveIndex

Returns an absolute index from a relative one.

Relative indexes differ from absolute ones in that they can be negative and
in those cases it would be as simple as substracting them from the length of
the array from where they belong to obtain their absolute counterparts.

**Parameters**

-   `array` **[Array](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array)&lt;any>** 
-   `relativeIndex` **[number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)** 

Returns **[number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number)** 

## License

[MIT](LICENSE.txt) :copyright: **Jumpn Limited** / Mauro Titimoli (mauro@jumpn.com)
