# SYNOPSIS
A minimal query selector helper library.

# INSTALL
```bash
npm install hxoht/qs
```

# API
There are only two methods, `qs` and `qsa`.

`qs` is a short function that assumes document, but can take an optional
additional parameter that will specify scope of the selector's execution.

```js
const qs = (s, p) => (p || document).querySelector(s)
```

`qsa` is the same as above, but uses `.querySelectorAll` and will also
convert the NodeList into an array, providing at least an empty array if
there are no nodes found.

```js
const qsa = (s, p) => [...(p || document).querySelectorAll(s)]

```js
module.exports = { qs, qsa }
```
