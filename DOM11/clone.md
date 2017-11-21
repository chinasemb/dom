

```
<!doctype html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		#div1{width: 100px;height: 100px;background-color: pink}
		#div2{width: 100px;height: 100px;background-color: purple}
	</style>
</head>
<body>
	<div id="box">
		<input type="button" value="点击clone" id="btn">
		<div   id="div1"></div>
		<hr    id="hr1">
		<div   id="div2">
			<p>I am language!!!</p>
		</div>
	</div>
	<script>
		/*需求:
			当点击按钮的时候,将紫色方块克隆到分割线上面;

			cloneNode() //克隆某个元素
			注意:
				在克隆的时候,默认只克隆指定元素本身,不会克隆该元素下的所有子节点,子孙节点,在参数里面(true)默认是false,即可克隆子孙节点啦.
				*事件是不会被克隆的(也可以解决的)

		*/

		var btn = document.getElementById("btn");
		var pink = document.getElementById("div1");
		var purple = document.getElementById("div2");
		var box = document.getElementById("box");
		var hr = document.getElementById("hr1");

		btn.onclick = function(){

			var cloneElement = purple.cloneNode(true);
			console.log(cloneElement);
			box.insertBefore(cloneElement,hr);
		}
	</script>
</body>
</html>
```
![这里写图片描述](http://img.blog.csdn.net/20171121120746877?watermark/2/text/aHR0cDovL2Jsb2cuY3Nkbi5uZXQvS2FzZWthbGU=/font/5a6L5L2T/fontsize/400/fill/I0JBQkFCMA==/dissolve/70/gravity/SouthEast)

