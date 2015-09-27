# Map Legend

**Make your legend visible, and clearly linked to your data**, and if possible, expanded by default. For example, in Leaflet:

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

Link your legend to your data to make associations more apparent to users. For example: via an interactive mouseover, clickable popup, etc. Then, use intuitive symbology throughout your map to make your legend supplemental, instead of a necessity for visitors.
