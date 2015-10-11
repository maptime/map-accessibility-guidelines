# Mobile

**Think mobile first,** and don't assume all users have ready access to desktop or laptop computers.  Be aware that your users may only have Internet access via phones or other mobile devices.  In fact, as of 2013:
> "34% of cell internet users go online mostly using their phones, and not using some other device such as a desktop or laptop computer." -[Pew Research Center](http://www.pewinternet.org/fact-sheets/mobile-technology-fact-sheet)

Keep mobile users in mind when building accessible maps! Consider things like: element sizes, load time, simple look and feel, navigation experience, etc.

## Viewport
In your HTML you can insert a `meta name="viewport"` tag that changes the view of your website no matter the size of their browser (desktop or mobile).

For example, with Leaflet:  
```html
<!DOCTYPE html>
<html>

  <head>
    <!-- Viewport for all browser sizes, including mobile -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no" />
    <title>Map Title</title>
    <!-- CSS styling -->
    <style>
      html, body, #map-container {
      	height: 100%;
      	width: 100%;
      	overflow: hidden;
      }
      #map {
        width: auto;
        height: 100%;
      }
    </style>
  </head>

  <body>
  <!-- Map container to ensure the map takes up 100% of the width and height in the browser -->
  <div id="map-container">
    <!-- The map div, where the map resides -->
    <div id="map"></div>
  </div>
  </body>

</html>
```

Also, **don't ever set your map's div to be at 100% width**, or mobile users often can't scroll to any content below the map!  Especially be careful when using Bootstrap that it doesn't kick the map into a div with 100% width and lock users into "map nav prison".

## Media Queries
The `@media` rule is used to define different style rules for different media types/devices.

For example:  
```css
@media screen and (min-width: 480px) {
  body {
    background-color: lightgreen;
  }
}
```
In this example when the viewport, or screen size, is 480 pixels wide or larger, change the `background-color` to light green. Otherwise if the viewport is smaller than 480 pixels in width the `<body>`'s `background-color` will be unchanged.

## Innovation
At first designing an application to work on mobile devices seems overwhelming, but in time it can be really fun!

You can turn off particular functionality, add in structure/organization, or even change CSS styling to enhance a user's experience while viewing in mobile (Remember the **KISS** principle)!

For example, check out the [leaflet-sidebar GitHub repo](https://github.com/turbo87/leaflet-sidebar/), which lets you customize sidebar interactions based on a user's screen size.  Using this model, a desktop user would experience the following:
![desktop-user](https://cloud.githubusercontent.com/assets/5023024/10415141/a00f0462-6fb1-11e5-8b0a-4e41f183fadd.png)

While a mobile user would experience the following:  
<img style="-webkit-user-select: none;" src="https://cloud.githubusercontent.com/assets/5023024/10415140/a00d46c2-6fb1-11e5-8174-c0496c30af5b.png" width="297" height="502"><img style="-webkit-user-select: none;" src="https://cloud.githubusercontent.com/assets/5023024/10415142/a0119d08-6fb1-11e5-8784-54cf2bbafd6b.png" width="297" height="502">

Return to the [Best Practices](../BestPractices.md) homepage.
