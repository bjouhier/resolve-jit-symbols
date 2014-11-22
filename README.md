# resolve-jit-symbols
[![build status](https://secure.travis-ci.org/thlorenz/resolve-jit-symbols.png)](http://travis-ci.org/thlorenz/resolve-jit-symbols)

Resolves symbols for dynamic code generated by a JIT via a map file.

```js
var resolveJITSymbols = require('resolve-jit-symbols');
var map = fs.readFileSync(__dirname + '/test/fixtures/jit.map', 'utf8')
  
var resolver = resolveJITSymbols(map);
var res = resolver.resolve('0x38852ffd485a');
console.log(res);
```

```
{ address        : '38852ffd4640',
  size           : '54c',
  decimalAddress : 62144686933568,
  symbol         : 'LazyCompile    : *go' }
```

## Status

Needs tests.

## Installation

    npm install resolve-jit-symbols

## API


<!-- START docme generated API please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN docme TO UPDATE -->

<div>
<div class="jsdoc-githubify">
<section>
<article>
<div class="container-overview">
<dl class="details">
</dl>
</div>
<dl>
<dt>
<h4 class="name" id="JITResolver"><span class="type-signature"></span>JITResolver<span class="signature">(map)</span><span class="type-signature"> &rarr; {Object}</span></h4>
</dt>
<dd>
<div class="description">
<p>Instantiates a JIT resolver for the given map.</p>
</div>
<h5>Parameters:</h5>
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>map</code></td>
<td class="type">
<span class="param-type">String</span>
|
<span class="param-type">Array.&lt;String></span>
</td>
<td class="description last"><p>either a string or lines with space separated HexAddres, Size, Symbol on each line</p></td>
</tr>
</tbody>
</table>
<dl class="details">
<dt class="tag-source">Source:</dt>
<dd class="tag-source"><ul class="dummy">
<li>
<a href="https://github.com/thlorenz/resolve-jit-symbols/blob/master/index.js">index.js</a>
<span>, </span>
<a href="https://github.com/thlorenz/resolve-jit-symbols/blob/master/index.js#L3">lineno 3</a>
</li>
</ul></dd>
</dl>
<h5>Returns:</h5>
<div class="param-desc">
<p>the initialized JIT resolver</p>
</div>
<dl>
<dt>
Type
</dt>
<dd>
<span class="param-type">Object</span>
</dd>
</dl>
</dd>
<dt>
<h4 class="name" id="JITResolver::resolve"><span class="type-signature"></span>JITResolver::resolve<span class="signature">(hexAddress)</span><span class="type-signature"> &rarr; {Object}</span></h4>
</dt>
<dd>
<div class="description">
<p>Matches the address of the symbol of which the given address is part of.</p>
</div>
<h5>Parameters:</h5>
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>hexAddress</code></td>
<td class="type">
<span class="param-type">String</span>
|
<span class="param-type">Number</span>
</td>
<td class="description last"><p>the hexadecimal address of the address to check</p></td>
</tr>
</tbody>
</table>
<dl class="details">
<dt class="tag-source">Source:</dt>
<dd class="tag-source"><ul class="dummy">
<li>
<a href="https://github.com/thlorenz/resolve-jit-symbols/blob/master/index.js">index.js</a>
<span>, </span>
<a href="https://github.com/thlorenz/resolve-jit-symbols/blob/master/index.js#L40">lineno 40</a>
</li>
</ul></dd>
</dl>
<h5>Returns:</h5>
<div class="param-desc">
<p>info of the matching symbol which includes address, size, symbol</p>
</div>
<dl>
<dt>
Type
</dt>
<dd>
<span class="param-type">Object</span>
</dd>
</dl>
</dd>
</dl>
</article>
</section>
</div>

*generated with [docme](https://github.com/thlorenz/docme)*
</div>
<!-- END docme generated API please keep comment here to allow auto update -->

## License

MIT
