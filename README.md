# Fable Hello World

Hello World example using the F# to JavaScript compiler [Fable](http://fable.io/).

## Running

First install [F#](http://www.fsharp.org/) (on Mac OS X: `brew install mono`), then run `npm install` in this repository.

Build the client-side JavaScript bundle with `npm run build`.

Open `index.html` in a browser.

## Bundle size

```
$ js-size out/bundle.js
┌─────────────────┬─────────┐
│ Minified (gzip) │ 1.85 kB │
└─────────────────┴─────────┘
```

Fable uses certain ES2015 features that may [need to be polyfilled](http://fable.io/docs/compiling.html#Polyfill ) to work on older browsers, either using [code-js](https://github.com/zloirock/core-js) or with something like [Polyfill.io](https://polyfill.io/v2/docs/).

```
$ js-size node_modules/core-js/client/core.js
┌─────────────────┬─────────┐
│ Minified (gzip) │ 26.8 kB │
└─────────────────┴─────────┘
```
