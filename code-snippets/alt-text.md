# Alternative Text

Alternative text (`<alt>`) provides a textual alternative to non-text content in web pages (i.e. static maps, and/or images).

To sighted users, there is generally no usability change.  Unless they look at your HTML code or decide to load the page without loading the accompanying image files (for example, for users with limited mobile data plans), sighted users will generally not see the addition of alternative text.  However, alternative text can be extremely helpful for people who are blind and rely on a screen reader to have the content of the website read to them.

## Use  
Us alternative text to describe the **_content and function_** of each image on your page.  The goal is to providing a semantic meaning and description for each image.  Alternative text, incidentally, can also be used by search engines.

For example, if you have an image thumbnail of a regional park map you could label the image alternative text to reflect the content of the image:

```html
<!-- An example of alternative text within an html image tag -->
<img src="/images/park_map.png" alt="thumbnail of regional park map" width="400" height="800" border="0">
```
Screen readers will read the alternative text of images, if alt text is present and precedes the alternative text with the word "graphic." If the image is a link, the screen reader precedes the alternative text with "graphic link."  So, in the example above, a screen reader would read: "Graphic: thumbnail of regional park map".


## Empty tags  
In some cases, for images that serve no purpose beyond decoration, you may not need to add alternative text.  For example, if you have a decorate image of a girl that is being used simply to provide some visual appeal on a human health website, an alternative text of `<alt="girl">` isn't helpful for those with screen readers.

In this case, an empty alt tag may be the best option. Screen readers ignore images without alternative text and say nothing, but users can set their preferences to read the file name. For example:
```html
<!-- Sometimes an empty alternative text tag is the answer -->
<img src="/images/girl.png" alt="">
```

Return to the [Best Practices](../BestPractices.md) homepage.
