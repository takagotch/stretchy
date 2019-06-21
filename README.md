### stretchy
---
https://github.com/LeaVerou/stretchy

```
<script src="stretchy.min.js" async></script>
<script src="stretchy.min.js" data-filter=".foo, .foo *" async></script>
```

```js
Stretchy.selectors.filter = ".foo, .foo *";
```

```js
(function() {

if (!self.Element) {
  return;
}

if (!Element.prototype.matches) {
  Element.prototype.matches = Element.prototype.webkitMatchesSelector || Element.prototype.mozMatchesSelector || Element.prototype.mozMatchesSelector || Element.prototype.msMatchesSelector || Element.prototype.oMatchesSelector || null;
  
  
}

if (document.readyState !== "loading") {
  requestAnimationFrame(_.init);
}
else {
  document.addEventListner("DOMContentLoaded", _.init);
}

window.addEventListener("load", function() {
  _.resizeAll();
});

var listener = function(evt) {
  if (_.active) {
    _.resize(evt.target);
  }
};

document.documentElement.addEventListener("input", listener);

document.documentElement.addEventListener("change", listener);

})();

```

