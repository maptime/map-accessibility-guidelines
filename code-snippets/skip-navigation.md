### Allow users to skip repetitive elements on the page:
You should provide a method that allows users to skip navigation or other elements that repeat on every page. This is usually accomplished by providing a **"Skip to Main Content"** or **"Skip Navigation"** link at the top of the page which jumps to the main content of the page. The "Skip to" navigation allows those with screen readers to get to content easily instead of having to tab through many non-relevant pieces of information. **_Note: Half of skip links don't work as a CSS element of `display:none` disables the skip to content or the `<div id>` has changed over time._**

If you have data that can be displayed in a table that is provided with your map, you can created a **"Skip to Table"** option to your users.

In addition, ensure **all** content can be accessed without the use of a mouse, use `tab` and directional keys (`+`, `-`, `↑`, `↓`, `←`, and `→`) to test your application and/or map. **_An application should have as much of the same content available to the largest audience as possible._**
