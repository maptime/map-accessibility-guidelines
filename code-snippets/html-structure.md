# HTML Structure

## Organization
Organize your HTML's document structure so headings, lists, and other structural elements provide meaning and structure to web pages. Also, **_headings should never be empty_** as empty headings cannot be read by a screen reader.

Blind users with screen readers have a difficult time navigating through content when a solid document structure is not set in place. In addition to serving those that are blind, document structure helps organize a page for other users and helps you maintain the page in the future.

Headings are a key component as they are also read by search engines and can help direct **all** users to your site. Plus, good organization makes it easier to update your code, especially during refactoring.

## Table Headers
Avoid using empty headers, especially within tables, as this will confuse screen readers, and be harder for you if you need to refactor these areas in your code.

Instead, add in context for your visitors:

```html
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
```

## Heading Levels
**_Don't skip heading levels._** Good document structure can also facilitate keyboard navigation within the page. Don't skip from a `<h1>` tag to a `<h3>` tag without using a `<h2>` tag in between the two.

**_However, you can skip backward_** For example, if you have already labeled your heading tags `<h1>`, `<h2>`, `<h3>`, and `<h4>` then you can skip to a `<h3>` tag without labeling the `<h1>` or `<h2>` tags since they are shown earlier in your code.

A good example of heading structure could be:  
```html
<!DOCTYPE html>
<html>
  <head>
    <title>Page Title</title>
  </head>
  <body>

    <h1>My First Heading</h1>
    <h2>My first Sub-Heading</h2>
    <h2>My second Sub-Heading</h2>

    <h1>My Second Heading</h1>

    <h1>My Third Heading</h1>
    <h2>My third Sub-Heading</h2>
    <h3>My first "Sub" Sub-Heading</h3>
    <h2>My fourth Sub-Heading</h2>

  </body>
</html>
```
