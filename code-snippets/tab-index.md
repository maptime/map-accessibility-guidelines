# Tab Index  
Tab index (`tabindex`) indicates if an element can take input focus, if it should participate in sequential keyboard navigation, and if so, at what position.

The `tabindex` attribute should only be used in cases where:  
  * The default tab order is not ideal, **AND**  
  * The tab order cannot be changed by rearranging items in the content and/or by altering the style sheet to reflect the best visual arrangement.  

When used, it can take several values, including:  

## 1. Tab Index = 0  
* Special meaning, and provides distinct functionality in HTML.  
* Allows elements besides links and form elements to receive keyboard focus, such as: `<div>`, `<span>`, and `<p>` elements.  
* It does not change the tab order, but places the element in the logical navigation flow, as if it were a link on the page.  

For example:  

```html  
<!-- Map div example: You could add your map div as a tabbed element within your page -->  
<div id="map" tabindex="0">  
```  

## 2. Tab Index = -1  
* Like `tabindex="0"`, provides special meaning and distinct functionality in HTML.  
* Can receive "programmatic" focus, meaning focus can be set to the element through scripting, links, etc. For example using `element.focus()`. However it can’t be reached by someone using the `tab` key to navigate through content.    
* **Removes the element from the default navigation flow** and allows it to receive programmatic focus. This means the focus can be set to it from a link, or with scripting.  
* **Do not use to any element that must be keyboard navigable**, such as a link or button that sighted users can click on with the mouse.  

For example:  
```html  
<!-- Skip to link example: If you implement a "skip to" section in your map you can disable
the default tabbing option for the user, but programmatically send a user to the area if
they click the "skip to" link -->  

<!-- Skip to link, shown only to screen readers and on focus -->
<a class="sr-only sr-only-focusable" href="#main">Skip to main content</a>  

<!-- Content where you can set programmatic focus, but a user can't tab to this area -->
<!-- A good example is if you have a div set up to view Google Map Street View images, that a screen reader wouldn't have interest in. -->
<div role="group" id="googleMapStreetView" aria-labelledby="Google Map Street View" tabindex="-1">
  <h2>Street View</h2>
</div>
```   

## 3. Tab Index >= 1
* Defines an explicit tab order. **This is almost always a bad idea.**  
* If used, any elements on the page with a `tabindex` greater than 1 will receive keyboard focus before elements with no `tabindex` value, or `tabindex='0'`.  
* If at all possible, do not use positive `tabindex` values. Instead, **fix the navigation order by restructuring the HTML.**   

For example:   
```html   
<!-- Unordered tabindex list example using basemap layers & 'feature' layers:  The structured order
will be seen visually, and read initially by screen readers in the same manner. However, if a user
tabs through the page, they will see/hear a different order. This behavior can create confusion to
screen reader users who are presented with two different page orders, one when reading the page,
and a second one when navigating using the tab key. -->  

<ul>  
  <li>Streets</li>  
  <li>Aerial imagery</li>  
  <li>Hybrid</li>  
  <li tabindex="1">Hotels</li>  
  <li tabindex="2">Attractions</li>  
  <li tabindex="3">Establishments</li>  
</ul>  
```  
Return to the [Best Practices](../BestPractices.md) homepage.
