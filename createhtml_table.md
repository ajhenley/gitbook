<!--djw:done-->
###HTML Tables

The HTML table tag allows you to arrange data like text, images, links in rows and columns of cells. Tables begin with a ```<table>``` tag and end with a ```</table>``` tag. Each row is between ```<tr> ... </tr>```. Each cell or data point is between ```<td> ... </td>``` tags. If you want a table header for the first row then use ```<th> ... </th>``` instead of ```<td> ... </td>```.

**Note: ** It is not considered appropriate to use tables to create rows and columns to render content layout. This is because screen readers assume tables contain data and read them row by row. Did you use tables for format your fabulous three column newsletter about wine? It will sound like you had to much of it to the person viewing your site with a screen reader. 

Example table:
```html
<table border="1" style="width:100%"  cellpadding="1" cellspacing="1">
  <thead>
  <tr><th>Year</th><th>Make</th><th>Model</th><th>Color</th></tr>
  </thead>
  <tbody>
  <tr><td>1999</td><td>Chevy</td><td>Corvette (small)</td><td>Red</td></tr> 
  <tr><td>1981</td><td>Renault</td><td>Barchetta</td><td>Red</td></tr> 
  <tr><td>1981</td><td>GM</td><td>Cadillac</td><td>Pink</td></tr> 
</tbody>
</table>
```



####Your Assignment
Create an HTML Table to display the following data:

<table cellpadding="1" cellspacing="1">
<tr>
	<th>First Name</th>
	<th>Last Name</th>
	<th>Phone</th>
</tr>
<tr>
	<td>Maryam</td>
	<td>Henry</td>
	<td>347-694-8645</td>
</tr>
<tr>
	<td>Amelia</td>
	<td>Cannon</td>
	<td>748-534-6259</td>
</tr>
<tr>
	<td>Hilel</td>
	<td>Watts</td>
	<td>736-712-0782</td>
</tr>
<tr>
	<td>Portia</td>
	<td>Hampton</td>
	<td>728-690-5531</td>
</tr>
<tr>
	<td>Cameran</td>
	<td>Kline</td>
	<td>775-470-2885</td>
</tr>
<tr>
	<td>Ashton</td>
	<td>Dickerson</td>
	<td>417-859-1589</td>
</tr>
<tr>
	<td>Sopoline</td>
	<td>Flowers</td>
	<td>445-198-8160</td>
</tr>
<tr>
	<td>Reese</td>
	<td>Huffman</td>
	<td>491-627-6062</td>
</tr>
<tr>
	<td>Hanna</td>
	<td>Wheeler</td>
	<td>975-850-0929</td>
</tr>
</table>
