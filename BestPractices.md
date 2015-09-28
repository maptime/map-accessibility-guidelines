# Best Practices in Cartographic Accessibility  

It is estimated that 20% of the population has a disability with 8.5% of the population having a disability that directly impacts their use on a computer. While not all disabilities make Internet use difficult for these populations a large proportion of people are affected in some way.

For schools, universities, and government organizations it would not only be unwise to avoid these populations, but in many cases, it would also violate the law while designing content for public consumption.

However, best practices in accessibility can impact **all** users in a good way. For example, Apple's iPhone has been designed with accessibility in mind but has created a better experience for all of its users over time.

**Web accessibility benefits everybody.** Your map or site can be compliant and technically accessible yet functionally inaccessible. Just because your map and/or website is accessible **_does not_** mean that is it usable. Ensure your content is usable first, then focus on making it accessible to your audience. Accessibility is not a barrier to innovation, design constraints will give you new ideas to explore that will lead to better products for your audience.

**It's an imperfect world; if your goal is 100% total accessibility before you begin, you have already failed.** Perfection is unattainable but *do the best of your ability* to make content available to the widest selection of users as possible. To do so, consider accessibility and usability as part of the same conversation.

Listed below is a set of guidelines for developers, cartographers, GIS specialists, geographers, and civic hackers to consider when creating projects that include static and interactive web maps.


## Table of Contents:
- **[Key principles](#section1)** for starting conversations about accessibility
- **[Accessibility techniques](#section2)** & code snippets


<a name="section1">
## Key principles for starting conversations about accessibility
</a>

* Focus on the purpose of the map, what story are you trying to tell?  Simplicity is best.  Keep asking: Does everybody need this?

* Make accessibility a developer-side concern.  Start this conversation from the very beginning of a project—don’t make it an afterthought.  Consider "accessibility" and "usability" as part of the same conversation.

* Design for a diverse set of users who will interact with your map(s).  Consider users including visually impaired users, users with cognitive disabilities, users with physical or motor limitations, users with different spatial perceptions, etc.  *Note:* Keyboard user != Screen reader user, but Keyboard user ≈ Screen reader user.

* Acquaint yourself with accessibility standards (WebAIM, etc.), but remember accessibility is about people. Only people can evaluate true accessibility. Accessibility evaluation tools (WAVE, etc.) can help facilitate human interaction but it is not the catch-all answer.

* Something that is dead on mobile, is dead.

* Enable the experience, don't make the experience.  

* If there's something you can't make accessible according to standards, first decide whether you really need it.  Consider how you might redesign it now, or take time do some background work and schedule it into a future release.  

* Accessibility is not a barrier to innovation.  It's an opportunity to share great map experiences with more users!


<a name="section2"/>  
## Accessibility techniques & code snippets
</a>

* **[Add a table and/or list](/code-snippets/add-table-or-list.md)**: Don’t have the map be your only format for data display, supplement it with a table and/or list (i.e. directions/routing, data display, etc.).
* **[Alternative text](/code-snippets/alt-text.md)**: Provide a textual alternative to non-text content in web pages (i.e. static maps, and/or images).
* **[Color](/code-snippets/color.md)**: Use contrast, texture, and human behaviors to enable and enhance visual user interaction.
* **[Focus](/code-snippets/focus.md)**: A focus can enhance an experience for all users and is a great best practice to use.
* **[HTML structure](/code-snippets/html-structure.md)**: Organize HTML document structure so headings, lists, and other structural elements provide meaning and structure.
* **[JavaScript](/code-snippets/javascript.md)**: The hover and focus responses should have the same functionality throughout an application.
* **[Links](/code-snippets/links.md)**: Every link should make sense out of context.
* **[Map legend](/code-snippets/map-legend.md)** Make your legend visible, and clearly linked to your data.
* **[Miscellaneous snippets](/code-snippets/miscellaneous.md)**: Miscellaneous code snippets to help you along the way!
* **[Mobile](/code-snippets/mobile.md)**: Think mobile first! Remember, anything dead on mobile, is dead.
* **[Non-HTML content](/code-snippets/non-html-content.md)**: Ensure accessibility of non-HTML content (e.g. PDF's, Microsoft Word documents, etc.).
* **[Skip navigation](/code-snippets/skip-navigation.md)** (e.g. Skip to content/table): Allow users to skip repetitive elements on the page and get to the reason they visit your page, aka the good stuff!
* **[Table headers](/code-snippets/table-headers.md)**: Provide titles and/or headers for data tables to provide context to users.
