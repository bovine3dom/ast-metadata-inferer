ast-metadata-inferer
======================
[![Build Status](https://travis-ci.org/amilajack/ast-metadata-inferer.svg?branch=master&maxAge=2592)](https://travis-ci.org/amilajack/ast-metadata-inferer) [![Greenkeeper badge](https://badges.greenkeeper.io/amilajack/ast-metadata-inferer.svg)](https://greenkeeper.io/)

A collection of metadata about browser API's. This collection is intended for tools that analyze javascript.

For all the API's it supports, it gives the
* AST node type of the API (`MemberExpression`, `NewExpression`, or `CallExpression`)
* If the API is statically invoked
* The kind of API it is

**⚠️ NOTE: HIGHTLY EXPERIMENTAL. DO NOT USE ️️⚠️**

## Example
```js
import AstMetadata from 'ast-metadata-inferer';

console.log(AstMetadata.find(record => record.protoChainId === 'document.querySelector'))
// {
//   "apiType":"js-api",
//   "type":"js-api",
//   "protoChain":["document","querySelector"],
//   "protoChainId":"document.querySelector",
//   "astNodeType":["MemberExpression"],
//   "isStatic":true
// }
```

## Importing Internals
```js
import { AssertionFormatter } from 'ast-metadata-inferer/lib/helpers/AstNodeTypeTester';

AssertionFormatter({ ... });
```
