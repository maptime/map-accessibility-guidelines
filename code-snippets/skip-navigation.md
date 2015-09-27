# Skip Navigation

**Allow users to skip repetitive elements on the page.** You should provide a method that allows users to skip navigation or other elements that repeat on every page.

## Skip to Main Content
This is usually accomplished by providing a **"Skip to Main Content"** or **"Skip Navigation"** link at the top of the page which jumps to the main content of the page.

The "Skip to" navigation allows those with screen readers to get to content easily instead of having to tab through many non-relevant pieces of information.

**_Note:_** Half of skip links don't work as a CSS element of `display:none` disables the skip to content or the `<div id>` has changed over time.

```html
<body>
<a href="#main-content">Skip to main content</a>

  <div id="main-content">
  </div>

</body>
```

## Skip to Table

If you have data that can be displayed in a table that is provided with your map, you can created a **"Skip to Table"** option to your users.

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
