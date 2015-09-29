# Mobile

**Think mobile first,** *and don't assume all users have ready access to desktop or laptop computers.*

Be aware that your users may only have Internet access via phones or other mobile devices. Keep them in mind when building accessible maps! **Do consider:** size, load time, look, experience, and use.

In fact, as of 2013:
> "34% of cell internet users go online mostly using their phones, and not using some other device such as a desktop or laptop computer." -[Pew Research Center](http://www.pewinternet.org/fact-sheets/mobile-technology-fact-sheet)

In your HTML you can insert a `meta name="viewport"` tag that changes the view of your website no matter the size of their browser (desktop or mobile).

For example, with Leaflet:  
```html
<!DOCTYPE html>
<html>

  <head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no" /><!-- Viewport for all browser sizes, including mobile -->
    <title>Map Title</title>
    <!-- CSS styling --><style>
      html, body, #map-container {
      	height: 100%;
      	width: 100%;
      	overflow: hidden;
      }
      #map {
        width: auto;
        height: 100%;
      }
    </style><!-- / CSS styling -->
  </head>

  <body>
  <div id="map-container"><!-- Map container to ensure the map takes up 100% of the width and height in the browser -->
    <div id="map"></div> <!-- The map div, where the map resides -->
  </div>
  </body>

</html>
```

**_Note_**: Don't ever let your map's div be at 100% width, or mobile users often can't scroll to any content below the map!  (Especially be careful when using Bootstrap that it doesn't kick the map into 100% width and lock users into "map nav prison".)

Return to the [Best Practices](../BestPractices.md) homepage.
