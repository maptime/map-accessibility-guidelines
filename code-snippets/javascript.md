# JavaScript

## Accessibility
Make your best effort to ensure that [JavaScript event handlers](http://webaim.org/techniques/javascript/eventhandlers) are device independent (i.e. events do not require the use of a mouse) and that your page does not rely on JavaScript to function.

**_Note:_** This is not always possible with interactive maps but make your best effort while designing your map if other alternatives are possible.

For example:  
```javascript
$('#target').on('click hover', function () {
    // JavaScript goes here
});
```

## Focus & Hover
**Don't make people hover to find things.** The hover and focus should have the same functionality throughout an application. It is important to try to maintain the following for your visitors: **_simple things should be simple, complex things should be possible._**

For example:
```css
:hover, :focus {
	/* CSS goes here */
}
```

## Tap
If you turn off pan, zoom, and other mouse/keyboard functionality don't forget to disable the `tap` handler as well to create a similar experience with touch devices.

For example:
```javascript
// Disable drag and zoom handlers.
map.dragging.disable();
map.touchZoom.disable();
map.doubleClickZoom.disable();
map.scrollWheelZoom.disable();

// Disable the tap handler, if present.
if (map.tap) map.tap.disable();
```

Return to the [Best Practices](../BestPractices.md) homepage.
