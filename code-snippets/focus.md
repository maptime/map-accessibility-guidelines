### Use focus to enhance the experience for all users. Don't remove focus for any users:

**Focus**:  A **great best practice to use.** A way to make your user experience similar for *many* different visitors is to provide visual focus indication for keyboard focus.
	- The default focus may need to be changed if it cannot be seen *clearly* by a user. Sometimes adding a border to the CSS, including changing the color goes a long way (e.g. `:focus { border: 2px dotted #000; }`)
	- Set the hover and focus CSS transitions equal to each other (`:hover, :focus`). The hover and focus should have the same functionality throughout an application.


**Outline**: Avoid using the following CSS as it will affect blind audiences visiting your site. `a { outline: 0; }` or  `a { outline: none; }`
