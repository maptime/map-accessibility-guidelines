# Skip Navigation

**Allow users to skip repetitive elements on the page.** You should provide a method that allows users to skip navigation or other elements that repeat on every page.

![skipper-gilligans-island](http://images4.fanpop.com/image/photos/20600000/Alan-Hale-Jr-as-Skipper-gilligans-island-20605756-380-304.jpg)

## Skip to Main Content
This is usually accomplished by providing a **"Skip to Main Content"** or **"Skip Navigation"** link at the top of the page which jumps to the main content of the page.

For example:
![skip-to-main-content](https://cloud.githubusercontent.com/assets/5023024/10154313/4f89633c-662b-11e5-935b-5e353fe1fb2c.png)

The "Skip to" navigation allows those with screen readers to get to content easily instead of having to tab through many non-relevant pieces of information.

**_Note:_** Half of skip links don't work as a CSS element of `display:none` disables the skip to content or the `<div id>` has changed over time.

To enable, you could use some of the following html:
```html
<body>
<a href="#main-content">Skip to main content</a>

  <div id="main-content">
  </div>

</body>
```

## Skip to Table

If you have data that can be displayed in a table that is provided with your map, you can created a **"Skip to Table"** option to your users.

For example:
![skip-to-table](https://cloud.githubusercontent.com/assets/5023024/10154228/8a7195b0-662a-11e5-8d9d-9f38e6ca5eb1.png)

To enable, you could use some of the following html:
```html
<body>
<a href="#data-table">Skip to table</a>

  <div id="data-table">
  </div>

</body>
```

## General Accessibility

In addition, ensure **all** content can be accessed without the use of a mouse, use `tab` and directional keys (`+`, `-`, `↑`, `↓`, `←`, and `→`) to test your application and/or map. **_An application should have as much of the same content available to the largest audience as possible._**

Return to the [Best Practices](../BestPractices.md) homepage.
