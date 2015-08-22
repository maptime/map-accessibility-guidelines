# Best Practices in Cartographic Accessibility  

It is estimated that 20% of the population has a disability with 8.5% of the population having a disability that directly impacts their use on a computer. While not all disabilities make internet use difficult for these populations a large proportion of people are affected in some way. 

For schools, universities, and government organizations it would not only be unwise to avoid these populations, but in many cases, it would also violate the law while designing content for public consumption.

However, best practices in accessibility can impact **_all_** users in a good way. For example, Apple's iPhone has been designed with accessibility in mind but has created a better experience for all of its users over time.

Listed below is a set of guidelines for developers, cartographers, GIS specialists, geographers, and civic hackers to consider when creating projects that include static and interactive web maps.

## Introduction:
**_Web accessibility benefits everybody._** Your map or site can be compliant and technically accessible yet functionally inaccessible. Just because your map and/or website is accessible **_does not_** mean that is it usable. Ensure your content is usable first, then focus on making it accessible to your audience. Accessibility is not a barrier to innovation, design constraints will give you new ideas to explore that will lead to better products for your audience.

**_It's an imperfect world; if your goal is 100% total accessibility before you begin, you have already failed:_** Perfection is unattainable but do *the best of your ability* to make content available to the widest selection of users as possible. To do so, consider accessibility and usability as part of the same conversation.


### Table of Contents:
- [Section I. Key Takeaways](#section1)
- [Section II. Accessibility Principles](#section2)
- [Section III. Accessibility Techniques](#section3)


<a name="section1">
## Section I. Key Takeaways:</a>
1. Focus on the purpose of the map, what story are you trying to tell? 
2. Design for a diverse set of users who will interact with your map(s).
3. Something that is dead on mobile, is dead. 
4. Accessibility is not a barrier to innovation. Think usability first, accessibility next.  
5. Simplicity is best, don't force it. Keep asking: Does everybody need this?
6. Accessibility is about people. Only people can evaluate true accessibility. WAVE can help facilitate human interaction but it is not the catch-all answer.  
7. Enable the experience, don't make the experience.  
8. Keyboard user != Screen reader user, but Keyboard user ≈ Screen reader user.
9. There are some things you just can't make accessible.


<a name="section2"/>  
## Section II. Accessibility Principles:</a>
#### 1. Assign alternative text *[static and interactive maps]*:
Alternative text provides a textual alternative to non-text content in web pages (i.e. static maps, and/or images). Alternative text is especially helpful for people who are blind and rely on a screen reader to have the content of the website read to them.

When using alternative text, describe the **_content and function_** providing a semantic meaning and description of the images, which is also used by search engines. For example, if you have a thumbnail of a regional park map you could label the image alternative text to reflect the content of the image (i.e. `<alt="Regional park map">`).

However, not all images are as clear cut. For example, if you have an image of a girl that is being used as context of human health an alternative text of `<alt="girl">` isn't helpful for those with screen readers. In fact, there is no right answer in this case as it is difficult to provide content and/or function to a screen reader so in the case `<alt="">` may be the best option.

#### 2. Implement an appropriate document structure *[interactive maps]*:
Headings, lists, and other structural elements provide meaning and structure to web pages. Also, **_headings should never be empty_** as empty headings cannot be read by a screen reader. Headings are a key component as they are also read by search engines and can help direct **all** users to your site.

**_Don't skip heading levels:_** The document structure can also facilitate keyboard navigation within the page. For example, don't skip from a `<h1>` tag to a `<h3>` tag without using a `<h2>` tag in between the two. Blind users with screen readers have a difficult time navigating through content when a solid document structure is not set in place. In addition to serving those that are blind, document structure helps organize a page for other users and helps you maintain the page in the future. 

**_However, you can skip backward_** For example, if you have already labeled your heading tags `<h1>`, `<h2>`, `<h3>`, and `<h4>` then you can skip to a `<h3>` tag without labeling the `<h1>` or `<h2>` tags since they are shown earlier in your code.

#### 3. Provide titles and/or headers for data tables *[static and interactive maps]*:
Try and refrain from using tables as a layout and use them **_strictly_** to display data that are **logical** and **intuitive**. Tables that are used to organize tabular data should have appropriate table headers (the `<th>` element). For example:

<table>
<caption>Shelly's Daughters</caption>
<tr>
<th scope="col">Name</th>
<th scope="col">Age</th>
<th scope="col">Birthday</th>
</tr>
<tr>
<th scope="row">Jackie</th>
<td>5</td>
<td>April 5</td>
</tr>
<tr>
<th scope="row">Beth</th>
<td>8</td>
<td>January 14</td>
</tr>
</table>

Data cells should be associated with their appropriate headers, making it easier for screen reader users to navigate and understand the data table using `scope` in the table headers and values. For example:

	<table>  
	<caption>Shelly's Daughters</caption>  
	<tr>  
	<th SCOPE="col">Name</th>  
	<th SCOPE="col">Age</th>  
	<th SCOPE="col">Birthday</th>  
	</tr>  
	<tr>  
	<th SCOPE="row">Jackie</th>  
	<td>5</td>  
	<td>April 5</td>  
	</tr>  
	<tr>  
	<th SCOPE="row">Beth</th>  
	<td>8</td>  
	<td>January 14</td>  
	</tr>  
	</table> 

#### 4. Ensure links make sense out of context *[interactive maps]*:
Every link should make sense if the link text is read by itself. Screen reader users may choose to read only the links on a web page. Certain phrases like "click here" and "more" **_must_** be avoided.  

#### 5. Ensure accessibility of non-HTML content (e.g. PDF files, forms, Microsoft Word documents, and PowerPoint presentations) *[static maps]*:
In addition to all of the other principles, PDF documents, forms, and other non-HTML content **_must be as accessible as possible_**. 

If you cannot make it accessible, consider using HTML instead or, at the very least, provide an accessible alternative. PDF documents and forms should also include a series of labels, with organization, to make it more accessible. A PDF file with labels looks the same, but it is almost always more accessible to a person using a screen reader.

#### 6. Allow users to skip repetitive elements on the page *[interactive maps]*:
You should provide a method that allows users to skip navigation or other elements that repeat on every page. This is usually accomplished by providing a **"Skip to Main Content"** or **"Skip Navigation"** link at the top of the page which jumps to the main content of the page. The "Skip to" navigation allows those with screen readers to get to content easily instead of having to tab through many non-relevant pieces of information. **_Note: Half of skip links don't work as a CSS element of `display:none` disables the skip to content or the `<div id>` has changed over time._**   

If you have data that can be displayed in a table that is provided with your map, you can created a **"Skip to Table"** option to your users.

In addition, ensure **all** content can be accessed without the use of a mouse, use `tab` and directional keys (`+`, `-`, `↑`, `↓`, `←`, and `→`) to test your application and/or map. **_An application should have as much of the same content available to the largest audience as possible._**


#### 7. Do not use color as the only visual means of conveying information *[static and interactive maps]*:
While we use color to highlight or compliment what is already visible, do not use color alone to convey information. That information may not be available to a person who is colorblind and will be unavailable to screen reader users. 

**_Contrast impacts everybody_**. Ensure sufficient contrast exists between text and its background. Common sense is vital when considering color contrast, if you can't differentiate the colors - nobody else will.

In order to showcase additional meaning, you can:

- Use simple, high-contrast color schemes.  
- Consider patterns, line widths, etc.
  
#### 8. Ensure content is clearly shown and/or written and easy to read *[static and interactive maps]*:

- Write clearly 
- Use [clear fonts](http://webaim.org/techniques/fonts), *WebAIM resource*
- Use [headings and lists](http://webaim.org/techniques/semanticstructure) appropriately, *WebAIM resource*


#### 9. Make sure content is clearly shown *[static and interactive maps]*:
- Number of layers:
	- Err on the side of too few layers (i.e. 3-4 per map). 
	- When in doubt, leave it out!
- Layer Zooming:
	- Display layer data in a way that is appropriate for the zoom level.
	- Hide and display geographic details as appropriate.

#### 10. Make JavaScript as accessible as possible *[interactive maps]*:
Make your best effort to ensure that [JavaScript event handlers](http://webaim.org/techniques/javascript/eventhandlers) are device independent (i.e. events do not require the use of a mouse) and that your page does not rely on JavaScript to function. (**_Note:_** This is not always possible with interactive maps but make your best effort while designing your map if other alternatives are possible).

**Don't make people hover to find things.** The hover and focus should have the same functionality throughout an application *([see code snippet below](#code1))*. Simple things should be simple, complex things should be *possible*.

#### 11. Design to standards *[static and interactive maps]*:
HTML-compliant and accessible pages are more robust and provide better search engine optimization. [Cascading Style Sheets](http://webaim.org/techniques/css) (CSS) allow you to separate content from presentation. This provides more flexibility and accessibility of your content.

#### 12. Supplement a visual display with a table or list *[static and interactive maps]*:
Remember that people have different ways of orienting themselves and absorbing geographic information, including percieving space and spatial concepts. **Don't let the map be your only format for data display**, supplement your map with a table and/or list (i.e. directions/routing, data display, etc.).

Adding additional content in the form of a table or list for users also provides another resource to blind, and even colorblind users when maps are involved. In this way a larger proportion of your audience can benefit from the content you are displaying, including users who may not be visually impaired at all.


#### 13. Color matters! *[static and interactive maps]*:
**People see color before they absorb anything else**. Many of the most recognizable brands in the world rely on color for instant recognition. 

Color plays an incredibly important role in the world and can sway thinking, change actions, and cause reactions. It can irritate or soothe one's eyes, raise blood pressure, or even suppress appetite. As a powerful form of communication, color is irreplaceable. For example: Red means *stop* and green means *go*. Likewise, as seen in the image below, the colors used for a product, web site, business card, or logo cause powerful reactions (especially when flipped!).

![yahoo-google-icon](https://cloud.githubusercontent.com/assets/5023024/8877212/dea3ca6a-31e9-11e5-969c-2ca63a5e2982.png)


#### 14. Think Mobile First! *[static and interactive maps]*:
**Don't assume all users have ready access to desktop or laptop computers.** Be aware that your users may only have Internet access via phones or other mobile devices.  Keep them in mind when building accessible maps!

In fact, as of 2013:
> "34% of cell internet users go online mostly using their phones, and not using some other device such as a desktop or laptop computer." -[Pew Research Center](http://www.pewinternet.org/fact-sheets/mobile-technology-fact-sheet) 

<a name="section3"/>  
## Section III: Accessibility Techniques:</a>

#### Code Snippets:

1. **Outline**: Avoid using the following CSS as it will affect blind audiences visiting your site. `a { outline: 0; }` or  `a { outline: none; }`
2. **Headers**: Avoid using empty headers (`<th>`).
3. <a name="code1"/>  **Focus**</a>:  A **great best practice to use.** A way to make your user experience similar for *many* different visitors is to provide visual focus indication for keyboard focus.
	- The default focus may need to be changed if it cannot be seen *clearly* by a user. Sometimes adding a border to the CSS, including changing the color goes a long way (e.g. `:focus { border: 2px dotted #000; }`)
	- Set the hover and focus CSS transitions equal to each other (`:hover, :focus`). The hover and focus should have the same functionality throughout an application.
4. **Leaflet Accessible Zoom Control**:  

	*CSS:*
    <pre>
	#zoom .easy-button-button {
	  transition-duration: .3s;
	  position: relative;
	  border-radius: 4px;
	  border: solid 0px transparent; }

	#zoom .easy-button-container{
	  background-color: white; }

	#zoom .zoom-btn{
	  position: absolute;
	  top: 0;
	  left: 0; }

	#zoom .easy-button-button.disabled {
	  height: 0; }
	</pre>

	*JavaScript*:
    
    ```javascript
	var userDefinedZoomMap = L.map('zoom', {zoomControl: false, scrollWheelZoom: false});

	L.tileLayer('http://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png').addTo(userDefinedZoomMap);

	// listeners for disabling buttons
	userDefinedZoomMap.on('zoomend',function(e){

	var map = e.target,
      max = map.getMaxZoom(),
      min = map.getMinZoom(),
      current = map.getZoom();

	if( current < max ){
		zoomIn.enable() }

	if( current >= max ){
		zoomIn.disable() }

	if( current > min ){
    	zoomOut.enable() }

	if( current <= min ){
    	zoomOut.disable() }

	});

	var plusUri = 'data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABoAAAAaCAYAAACpSkzOAAAABmJLR0QA/wD/AP+gvaeTAAAACXBIWXMAAAsTAAALEwEAmpwYAAAAB3RJTUUH3wYJFTodgbZtSwAAABl0RVh0Q29tbWVudABDcmVhdGVkIHdpdGggR0lNUFeBDhcAAABoSURBVEjHY2AYBaNg2AJmMvQkMTAwGDAwMHAzMDA8JlYTIxkW/SdHPxO9gm7kWWQNjRNkjB5fMPyXgYEhg1yL1Eh0tCm5FpGSKr/jUz+avOlq0Xco/Y8UTSxkWLQCGk+nR6uKUTC4AQC8oBHyYLAfhwAAAABJRU5ErkJggg=='
	
	var minusUri = 'data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABoAAAAaCAYAAACpSkzOAAAABmJLR0QA/wD/AP+gvaeTAAAACXBIWXMAAAsTAAALEwEAmpwYAAAAB3RJTUUH3wYJFgAjZzgQwAAAABl0RVh0Q29tbWVudABDcmVhdGVkIHdpdGggR0lNUFeBDhcAAAAvSURBVEjHY2AYBaNgFIyCUcDAwMAQzsDA8J8InIPPECZ6uZZpNMJGwSgYBSMAAADZ/wm/p4Wt3gAAAABJRU5ErkJggg=='
	
    var zoomIn = L.easyButton('<img class="zoom-in zoom-btn" src="'+ plusUri +'" alt="zoom in"/>',
                          function(control, map){map.setZoom(map.getZoom()+1);});
	var zoomOut = L.easyButton('<img class="zoom-out zoom-btn" src="' + minusUri + '" alt="zoom in"/>',
                           function(control, map){map.setZoom(map.getZoom()-1);});
    var zoomBar = L.easyBar([ zoomIn, zoomOut, ]);

	zoomBar.addTo(userDefinedZoomMap);

	userDefinedZoomMap.setView({lat:50, lng:0}, 2); 
	```

#### Samples of Accessible Maps:
*More samples coming soon!*

1. Minnesota Department of Health's MN Public Health Data Access (e.g. [Asthma Hospitalizations](https://apps.health.state.mn.us/mndata/webmap/asthma.html))

#### Before and After Samples:  
*Maps improved for accessibility (Coming soon)!*

#### Templates
*Coming soon!*
