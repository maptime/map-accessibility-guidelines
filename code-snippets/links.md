# Links
Every link should **_make sense out of context_**, even if the link text is read by itself. Screen reader users may choose to read only the links on a web page when they're trying to navigate quickly.

Certain phrases like **_"click here" and "more" must be avoided._** If we use phrases like 'click here' not only can it be confusing for those with screen readers (and repetitive, in some cases), we lose the attention of other visitors that are scanning our pages. By rewriting our links, we are helping **all audiences**!

**_Bad example_**:  
~~Click [here](http://www.github.com) to learn more!~~  

**_Good example_**:  
Learn more about [GitHub](http://www.github.com).  

```html
Learn more about <a href="http://www.github.com">GitHub</a>.
```  

## New Windows  
_When opening a link it is best to open it in the **same window, or tab**._ Opening a link in a new window, also known as `target="_blank"`, causes a few problems such as:  

* Screen reader users, and users with certain cognitive impairments can become disoriented when a new window is opened.  
* The back button, the most used button in the browser, is broken.  
* Some user agents, such as kiosks, can't open new windows, or tabs.  

However, there are times where it is appropriate to open a link in a new window, such as opening a map application.   _If you must open a link in a new window, you should alert the user._   

**Bad example:**  
~~Learn more about [GitHub](http://www.github.com).~~  

**Good example:**  
Learn more about [Github (new window)](http://www.github.com).   

```html
Learn more about <a href="http://www.github.com" target="_blank">GitHub (new window)</a>.
```


Return to the [Best Practices](../BestPractices.md) homepage.
