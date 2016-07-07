## Use `void 0` rather than `undefined` [Back](./../underscore.md)

If you look through the whole source code, you'll never find any `undefiend`, but only one string `"undefined"`, why?

Firstly, `undefined` is not a reversed word, and it's only a attribute of all global objects, which can be override in low edition of IE.

```js
var undefined = 10;

console.log(undefined); /**
                         * => undefined (Chrome)
                         * => 10        (IE 8)
                         */
```

In ES5, `undefined` has been designed as a **read-only** attributes, which can't be overriden. However, you will find that you can do it in a local scope:

```js
(function () {
})();

(function () {
})();
```


