# Miscellaneous Code Snippets

## Leaflet L.tileLayer
By default Leaflet's `L.tileLayer` does not include an `alt` tag and does **not** meet general web accessibility requirements. To ensure the tiles have an `alt` tag add in a Leaflet map listener (`tileloadstart`) and set the attribute (`alt`).

```javascript
//Basemap: Mapquest OSM
var mapquestOSM = L.tileLayer('https://otile1-s.mqcdn.com/tiles/1.0.0/{type}/{z}/{x}/{y}.{ext}', {
	type: 'map',
	ext: 'jpg',
	attribution: 'Tiles Courtesy of MapQuest &mdash; Map data &copy; OpenStreetMap',
	subdomains: '1234',
});

//Add an <alt> tag to the Leaflet tile layers on the initial tile load and when a tile load has started
mapquestOSM.on('tileloadstart', function (tileEvent) {
	tileEvent.tile.setAttribute('alt', 'Map tile image');
});
```

## Leaflet Accessible Zoom Control  

CSS:

```css
#zoom .easy-button-button {
  transition-duration: .3s;
  position: relative;
  border-radius: 4px;
  border: solid 0px transparent;
}

#zoom .easy-button-container{
  background-color: white;
}

#zoom .zoom-btn{
  position: absolute;
  top: 0;
  left: 0;
}

#zoom .easy-button-button.disabled {
  height: 0;
}
```

JavaScript:

```javascript
var userDefinedZoomMap = L.map('zoom', {
	zoomControl: false, scrollWheelZoom: false
});

L.tileLayer('http://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png').addTo(userDefinedZoomMap);

// listeners for disabling buttons
userDefinedZoomMap.on('zoomend',function(e){
	var map = e.target,
	    max = map.getMaxZoom(),
	    min = map.getMinZoom(),
	    current = map.getZoom();
		if( current < max ){
			zoomIn.enable()
		}
		if( current >= max ){
			zoomIn.disable()
		}
		if( current > min ){
			zoomOut.enable()
		}
		if( current <= min ){
			zoomOut.disable()
		}
});

var plusUri = 'data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABoAAAAaCAYAAACpSkzOAAAABmJLR0QA/wD/AP+gvaeTAAAACXBIWXMAAAsTAAALEwEAmpwYAAAAB3RJTUUH3wYJFTodgbZtSwAAABl0RVh0Q29tbWVudABDcmVhdGVkIHdpdGggR0lNUFeBDhcAAABoSURBVEjHY2AYBaNg2AJmMvQkMTAwGDAwMHAzMDA8JlYTIxkW/SdHPxO9gm7kWWQNjRNkjB5fMPyXgYEhg1yL1Eh0tCm5FpGSKr/jUz+avOlq0Xco/Y8UTSxkWLQCGk+nR6uKUTC4AQC8oBHyYLAfhwAAAABJRU5ErkJggg=='

var minusUri = 'data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABoAAAAaCAYAAACpSkzOAAAABmJLR0QA/wD/AP+gvaeTAAAACXBIWXMAAAsTAAALEwEAmpwYAAAAB3RJTUUH3wYJFgAjZzgQwAAAABl0RVh0Q29tbWVudABDcmVhdGVkIHdpdGggR0lNUFeBDhcAAAAvSURBVEjHY2AYBaNgFIyCUcDAwMAQzsDA8J8InIPPECZ6uZZpNMJGwSgYBSMAAADZ/wm/p4Wt3gAAAABJRU5ErkJggg=='

var zoomIn = L.easyButton('<img class="zoom-in zoom-btn" src="'+ plusUri +'" alt="zoom in"/>', function(control, map){
	map.setZoom(map.getZoom()+1);
});

var zoomOut = L.easyButton('<img class="zoom-out zoom-btn" src="' + minusUri + '" alt="zoom in"/>', function(control, map){
	map.setZoom(map.getZoom()-1);
});

var zoomBar = L.easyBar([ zoomIn, zoomOut, ]);

zoomBar.addTo(userDefinedZoomMap);

userDefinedZoomMap.setView({
	lat:50, lng:0
}, 2);
```

Return to the [Best Practices](../BestPractices.md) homepage.
