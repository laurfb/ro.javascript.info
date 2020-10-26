importance: 3

---

# Explicați valoarea variabilei "this"

<<<<<<< HEAD:1-js/04-object-basics/04-object-methods/3-why-this/task.md
În codul următor intenționăm să apelăm metoda `user.go()` de 4 ori la rând.
=======
In the code below we intend to call `obj.go()` method 4 times in a row.
>>>>>>> 2d5be7b7307b0a4a85e872d229e0cebd2d8563b5:1-js/99-js-misc/04-reference-type/3-why-this/task.md

Însă apelurile `(1)` și `(2)` funcționează diferit de `(3)` și `(4)`. De ce?

```js run no-beautify
let obj, method;

obj = {
  go: function() { alert(this); }
};

obj.go();               // (1) [object Object]

(obj.go)();             // (2) [object Object]

(method = obj.go)();    // (3) undefined

(obj.go || obj.stop)(); // (4) undefined
```