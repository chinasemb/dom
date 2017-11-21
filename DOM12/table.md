

```
<!doctype html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
</head>
<body>
	
		<table border="" id="box"> 
			<thead>
				<tr>
					<th>头一</th>
					<th>头二</th>
					<th>头三</th>
					<th>头四</th>
				</tr>
			</thead>
			<tbody>
				<tr>
					<td>内容一</td>
					<td>内容二</td>
					<td>内容三</td>
					<td>内容四</td>
				</tr>
				<tr>
					<td>内容一</td>
					<td>内容二</td>
					<td>内容三</td>
					<td>内容四</td>
				</tr>
				<tr>
					<td>内容一</td>
					<td>内容二</td>
					<td>内容三</td>
					<td>内容四</td>
				</tr>
				<tr>
					<td>内容一</td>
					<td>内容二</td>
					<td>内容三</td>
					<td>内容四</td>
				</tr>
			</tbody>
			<tbody>
				<tr>
					<td>内容一</td>
					<td>内容二</td>
					<td>内容三</td>
					<td>内容四</td>
				</tr>
				<tr>
					<td>内容一</td>
					<td>内容二</td>
					<td>内容三</td>
					<td>内容四</td>
				</tr>
				<tr>
					<td>内容一</td>
					<td>内容二</td>
					<td>内容三</td>
					<td>内容四</td>
				</tr>
				<tr>
					<td>内容一</td>
					<td>内容二</td>
					<td>内容三</td>
					<td>内容四</td>
				</tr>
			</tbody>
			<tfoot>
				<tr>
					<td>统计一</td>
					<td>统计二</td>
					<td>统计三</td>
					<td>统计四</td>
				</tr>
			</tfoot>
		</table>
	
	<script>
		/*  table.tHead    -->     获取tHead 
			table.rows     -->     获取tr
			table.tBodies  -->     获取body集合
			cells是单元格  

		*/
		var box = document.getElementById("box");
		box.tHead.style.borderColor = "red";
		console.log(box.rows);

		box.rows[1].style.backgroundColor ="pink";
		box.rows[2].style.backgroundColor ="greenYellow";
		box.rows[3].style.backgroundColor ="yellow";
		box.rows[4].style.backgroundColor ="blue";
		box.tBodies[0].style.background ="black";
		box.tBodies[1].style.background ="red";
		box.tFoot.style.backgroundColor="#ccc";
		box.tBodies[1].rows[1].cells[1].style.background="yellow";
	</script>
</body>
</html>
```

