# Focus

Use a focus to enhance the experience for all users, and it is a great practice to use. **Do not** remove the focus for any users!

![focus-like-a-cat](http://scienceinseconds.com/cmsFiles/pageImages/LolCatRenderer-20.jpg)

A way to make your user experience similar for *many* different visitors is to provide visual focus indication for keyboard focus.  An example of a focus in-action:  
![out](https://cloud.githubusercontent.com/assets/5023024/10264622/2a6861de-69d7-11e5-9e6d-b817d852ce2d.gif)

The default focus may need to be changed if it cannot be seen *clearly* by a user. Sometimes adding a border to the CSS, including changing the color goes a long way. For example:  
```css
:focus {
	border: 2px dotted #000;
}
```
* Set the hover and focus CSS transitions equal to each other as the hover and focus should have the *same functionality* throughout an application.  This makes the experience more unified for both keyboard and mouse users.  For example:
```css
:hover, :focus {
	/* CSS goes here */
}
```

## Avoid 'Outline' property
Do **_not_** use the following CSS in your website, as screen readers will be unable to navigate throughout your site:

```css
/* DO NOT use the following code in your CSS */
a {
	outline: 0;
}
a {
	outline:none;
}
```

Return to the [Best Practices](../BestPractices.md) homepage.
