# Table Headers

**Provide titles and/or headers for data tables.** Try to refrain from using tables as a layout and use them **_strictly_** to display data that are **logical** and **intuitive**.

Tables that are used to organize tabular data should have appropriate table headers (the `<th>` element).

Data cells should be associated with their appropriate headers, making it easier for screen reader users to navigate and understand the data table using `scope` in the table headers and values. The `scope` attribute identifies whether a table header is a column header or a row header enabling an experience for screen readers.

For example:

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

Return to the [Best Practices](../BestPractices.md) homepage.
