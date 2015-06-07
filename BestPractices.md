# Best Practices in Cartographic Accessibility

It is estimated that 20% of the population has a disability. While not all disabilities make internet use difficult for these populations a large proportion of people are affected in some way. For schools, universities, and government organizations it would not only be unwise to avoid these populations, but in many cases, it would also violate the law while designing content for public consumption.

Listed below is a set of guidelines for developers, cartographers, GIS specialists, geographers, and civic hackers to consider when creating projects that include static and interactive web maps.

## Introduction:
Just because your map and/or website is accessible **_does not_** mean that is it usable. Ensure your content is usable first, then focus on making it accessible to your audience. 

Perfection is unattainable but do **_the best of your ability_** to make content available to the widest selection of users as possible. To do so, consider accessibility and usability as part of the same conversation.


### Table of Contents:
- [Section I. How to Contribute to the Project](#section1)  
- [Section II. Project History](#section2)  
- [Section III. Types of Disabilities](#section3)  
- [Section IV. Accessibility Principles](#section4)
- [Section V. Accessibility Techniques](#section5)
- [Section VI. International Laws and Standards](#section6)  
- [Section VII. Resources](#section7) 



<a name="section1">
## Section I. How to Contribute to the Project:</a>
Send us a pull request if you have something to share! You can also contact us at [contact@opentwincities.org](mailto:contact@opentwincities.org) to be added as a contributor to this repository. 

We are especially interested in gathering: code snippets, templates, samples of accessible maps, guidelines, documentation, broader discussions on map accessibility, and much more!


<a name="section2"/>
## Section II. Project History:</a>
This project originated in February 2015 as part of the Hennepin County (MN) Geo:Code event. Other groups who have supported or contributed to this project include:

- [Open Twin Cities](http://opentwincities.org)
- [Maptime MSP](http://www.meetup.com/MaptimeMSP)
- *[Your name here...]*


<a name="section3" />
## Section III. Types of Disabilities:</a>

The four major categories of disability types are:

### 1. Visual:
Blindness, low-vision, color-blindness.

### 2. Hearing:
Deafness and hard-of-hearing.

### 3. Motor:
Inability to use a mouse, slow response time, limited fine motor control (i.e. Cerebral Palsy, complete paralysis).

### 4. Cognitive: 
Learning disabilities, distractibility, inability to remember or focus on large amounts of information.


<a name="section4"/>  
## Section IV. Accessibility Principles:</a>
#### 1. Assign alternative text *[static and interactive maps]*:
Alternative text provides a textual alternative to non-text content in web pages (i.e. static maps, and/or images). Alternative text is especially helpful for people who are blind and rely on a screen reader to have the content of the website read to them.

#### 2. Implement an appropriate document structure *[interactive maps]*:
Headings, lists, and other structural elements provide meaning and structure to web pages. The document structure can also facilitate keyboard navigation within the page. 

For example, don't skip from a `<h1>` tag to a `<h3>` tag without using a `<h2>` tag in between the two. Blind users with screen readers have a difficult time navigating through content when a solid document structure is not set in place. In addition to serving those that are blind, document structure helps organize a page for other users and helps you maintain the page in the future.

#### 3. Provide titles and/or headers for data tables *[static and interactive maps]*:
Try and refrain from using tables as a layout and use them **_strictly_** to display data. Tables that are used to organize tabular data should have appropriate table headers (the `<th>` element). For example:

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

#### 5. Ensure accessibility of non-HTML content (e.g. PDF files, Microsoft Word documents, and PowerPoint presentations) *[static maps]*:
In addition to all of the other principles, PDF documents and other non-HTML content **_must be as accessible as possible_**. 

If you cannot make it accessible, consider using HTML instead or, at the very least, provide an accessible alternative. PDF documents should also include a series of tags to make it more accessible. A tagged PDF file looks the same, but it is almost always more accessible to a person using a screen reader.

#### 6. Allow users to skip repetitive elements on the page *[interactive maps]*:
You should provide a method that allows users to skip navigation or other elements that repeat on every page. This is usually accomplished by providing a **"Skip to Main Content"** or **"Skip Navigation"** link at the top of the page which jumps to the main content of the page. The "Skip to" navigation allows those with screen readers to get to content easily instead of having to tab through many non-relevant pieces of information.

If you have data that can be displayed in a table that is provided with your map, you can created a **"Skip to Table"** option to your users.

#### 7. Do not rely on color alone to convey meaning *[static and interactive maps]*:
The use of color can enhance comprehension, but do not use color alone to convey information. That information may not be available to a person who is colorblind and will be unavailable to screen reader users.

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

#### 11. Design to standards *[static and interactive maps]*:
HTML-compliant and accessible pages are more robust and provide better search engine optimization. [Cascading Style Sheets](http://webaim.org/techniques/css) (CSS) allow you to separate content from presentation. This provides more flexibility and accessibility of your content.

#### 12. Supplement a visual display with a table or list *[static and interactive maps]*:
Remember that people have different ways of orienting themselves and absorbing geographic information. Don't let the map be your only format for data display, supplement your map with a table and/or list (i.e. directions/routing, data display, etc.).

Adding additional content in the form of a table or list for users also provides another resource to blind, and even colorblind users when maps are involved. In this way a larger proportion of your audience can benefit from the content you are displaying, including users who may not be visually impaired at all.


<a name="section5"/>  
## Section V: Accessibility Techniques:</a>
#### Code Snippets:
*Coming soon!*

#### Samples of Accessible Maps:
*Coming soon!*

#### Templates
*Coming soon!*


<a name="section6"/>  
## Section VI. International Laws and Standards:</a>
### Australia:
- [Disability Discrimination Act](http://www.austlii.edu.au/au/legis/cth/consol_act/dda1992264) (DDA) of 1992
- [World Wide Web Access: Disability Discrimination Act Advisory Notes](http://www.hreoc.gov.au/disability_rights/standards/www_3/www_3.html), version 3.2 *(August 2002)*

### Canada:
- [Canadian Human Rights Act](http://laws.justice.gc.ca/en/H-6/243963.html) of 1977
- [Ontarians with Disailities Act](http://www.e-laws.gov.on.ca/DBLaws/Statutes/English/01o32_e.htm) of 2001
- [Government of Canada Internet Guide](http://www.gol-ged.gc.ca/index_e.asp)
- [Canada's Common Look and Feel Guidelines](http://www.tbs-sct.gc.ca/clf-nsi/index_e.asp)
	- [Provisions for accessibility](http://www.tbs-sct.gc.ca/clf-nsi/inter/inter-01-tb_e.asp)

### Germany:
- [Federal Ordinance on Barrier-Free Information Technology](http://www.einfach-fuer-alle.de/artikel/bitv_english)

### Ireland:
- [Irish National Disability Authority IT Accessibility Guidelines](http://www.accessit.nda.ie/policy_and_legislation.html)

### Japan:
- [Web Access by People with Disabilities](http://www.legco.gov.hk/yr00-01/english/panels/itb/papers/a774-02e.pdf) *(March 12, 2001)*
- [Government concerns about enhancing web accessibility](http://www.info.gov.hk/gia/general/200109/30/0929144.htm), *Press release*
- [Basic Law on the Formation of an Advanced Information and Telecommunications Network Society](http://www.kantei.go.jp/foreign/it/it_basiclaw/it_basiclaw.html) *(January 6, 2001)*

### New Zealand:
- [E-Government Initiative of New Zealand](http://www.e-government.govt.nz/) (web guidelines)

### Portugal:
- [Accessibility of Public Administration Web Sites for Citizens with Special Needs](http://www.acesso.umic.pcm.gov.pt/acesso/res9799_en.htm)

### United Kingdom:
- [Disability Discrimination Act (DDA)](http://www.hmso.gov.uk/acts/acts1995/Ukpga_19950050_en_1.htm) of 1995
- [Accessibility as a legal requirement in UK](http://lists.w3.org/Archives/Public/w3c-wai-ig/2003JanMar/0022.html) *(October 1, 1999)*
- [Special Educational Needs and Disability Act](http://www.hmso.gov.uk/acts/acts2001/20010010.htm) of 2001
- [Disability Rights Commission (DRC) Code of Practice](http://www.drc-gb.org/uploaded_files/documents/2008_223_drc_cop_rights_of_Access.doc)

###United States of America: 
- [The Americans with Disabilities Act (ADA)](http://webaim.org/articles/laws/usa/ada)*, WebAIM summary*  
- [Rehabilitation Act of 1973](#)
	- [Section 504](http://www.dol.gov/oasam/regs/statutes/sec504.htm)
	- [Section 508](http://www.section508.gov)  


<a name="section7"/>  
## Section VII. Resources:</a>
### Cartography:
- *Coming soon!*

### Browser Extensions:
- Accessibility Developer Tools ([Chrome](https://chrome.google.com/webstore/detail/accessibility-developer-t/fpkknkljclfencbdbgkenhalefipecmb))
- ChromeVox ([Chrome](https://chrome.google.com/webstore/detail/chromevox/kgejglhpjiefppelpmljglcjbhoiplfn))
- Color Contrast Analyzer ([Chrome](https://chrome.google.com/webstore/detail/color-contrast-analyzer/dagdlcijhfbmgkjokkjicnnfimlebcll))
- ColorZilla (Firefox, [Chrome](https://chrome.google.com/webstore/detail/colorzilla/bhlhnicpbhignbdhedgjhgdocnmhomnp))
- NoCoffee ([Chrome](https://chrome.google.com/webstore/detail/nocoffee/jjeeggmbnhckmgdhmgdckeigabjfbddl))
- WAVE Evaluation Tool ([Chrome](https://chrome.google.com/webstore/detail/wave-evaluation-tool/jbbplnpkjmmeebjpijfedlgcdilocofh))

### Color Blindness:
- [Color Brewer](http://colorbrewer2.org) 
- [Color Oracle](http://www.colororacle.org) (software download)
- [Color Picker for Data](http://tristen.ca/hcl-picker)

### Color Contrast:
- [Colorable](http://jxnblk.com/colorable)
- [Tangaru Contrast-Finder](http://contrast-finder.tanaguru.com)

### General Web:
- [Accessibility in User-Centered Design Using Personas](http://www.uiaccess.com/accessucd/personas.html)
- [WebAIM](http://webaim.org)
- [Web Content Accessibility Guidelines](http://www.w3.org/TR/WCAG20) (WCAG 2.0)