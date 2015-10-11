# Map Legend

**Make your legend visible, and clearly linked to your data**, and if possible, expanded by default.

Some mapping libraries, such as Leaflet.js, do not have a legend expanded by default, even in larger browser windows.

<img width="49" alt="screenshot of Leaflet legend icon unexpanded" src="https://cloud.githubusercontent.com/assets/5023024/10264296/d560dbda-69cc-11e5-96ac-6e9f9ed0c742.png">

While a minimized legend can have its purpose on mobile displays, it is an asset on larger displays to ensure your visitors can understand your map.

Instead of using the default display, you can add in a few lines of code to expand your map legend on larger displays with the following code in Leaflet.js:

```javascript
/* Current as of Leaflet version 1.0.0 */

// Browsers larger than 767 pixels will see an expanded layer control
if (document.body.clientWidth <= 767) {
    isCollapsed = true;
} else {
    isCollapsed = false;
}

// Add the legend to the map
// Add the isCollapsed method to the legend
L.control.layers(baseMaps, overlayMaps, {
  	collapsed: isCollapsed
});
```

And, voila! You now have an expanded legend! :stuck_out_tongue_winking_eye:

<img width="224" alt="screenshot of Leaflet legend fully expanded" src="https://cloud.githubusercontent.com/assets/5023024/10264291/c0d4262c-69cc-11e5-8fec-865d704e56a0.png">

## Other Legend Tips
Link your legend to your data to make associations more apparent to users. For example: via an interactive mouseover, clickable popup, etc. Then, use intuitive symbology throughout your map to make your legend supplemental, instead of a necessity for visitors.

Return to the [Best Practices](../BestPractices.md) homepage.
