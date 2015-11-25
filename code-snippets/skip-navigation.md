# Skip Navigation

**Allow users to skip repetitive elements on the page**, which users can access by using the `tab` key on their keyboard. You should provide a method that allows users to skip navigation or other elements that repeat on every page.  This is particularly useful for users with screen readers, as it allows them to jump straight to the important content on a page without having to first navigate through the navigation bar and other repetitive links that commonly occur at the top of each web page.

![skipper-gilligans-island](http://images4.fanpop.com/image/photos/20600000/Alan-Hale-Jr-as-Skipper-gilligans-island-20605756-380-304.jpg)

## Skip to Main Content
This is usually accomplished by providing a **"Skip to Main Content"** or **"Skip Navigation"** link at the top of the page which jumps to the main content of the page.

For example:
![skip-to-main-content](https://cloud.githubusercontent.com/assets/5023024/10154313/4f89633c-662b-11e5-935b-5e353fe1fb2c.png)

The "Skip to" navigation allows those with screen readers to get to content easily instead of having to tab through many non-relevant pieces of information.

To enable, you could use some of the following html:
```html
<body>
<a href="#main-content">Skip to main content</a>

  <div id="main-content">
  </div>

</body>
```

**_Note:_** When making skip links, also make sure you don't hide them with CSS!  For example, *do not* set skip links as `display:none`; if you do this, they won't show up on your page.  Also try to label your skips links and the divs they target with generic enough names that you can recycle them across pages: for example, `<div id="#main-content">`.  This helps make sure your skip links don't break if you update specific divs within your page content over time.


## Skip to Table

If you have data that can be displayed in a table that is provided with your map, you can create a **"Skip to Table"** option for your users.

For example:
![skip-to-table](https://cloud.githubusercontent.com/assets/5023024/10264147/d9f85bda-69c9-11e5-99f1-dc6b3a5b4d71.gif)

To enable, you could use some of the following html:
```html
<body>
<a href="#data-table">Skip to table</a>

  <div id="data-table">
  </div>

</body>
```

## General Accessibility

In addition, ensure **all** content can be accessed without the use of a mouse, use `tab` and directional keys (`+`, `-`, `↑`, `↓`, `←`, and `→`) to test your application and/or map. **An application should have as much of the same content available to the largest audience as possible.**

Return to the [Best Practices](../BestPractices.md) homepage.
