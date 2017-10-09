Iron.Location
==============================================================================
Reactive urls that work with IE8/9 and modern pushState browsers.

Fork Changes:

* The click handler doesn't preventDefault() of anchors with the class "permit-anchor"
Intra-page a href tags should include that class in order to work correctly.
Previous versions of Iron.Location had no way to acheive that functionality.

## Example

```javascript
Deps.autorun(function () {
  // returns a "location" like object with all of the url parts
  var current = Iron.Location.get();

  var href = current.href;
  var state = current.state;
  var host = current.host;
  // etc
});
```
