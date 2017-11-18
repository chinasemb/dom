

```
<!doctype html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Document</title>
	<style>
		ul{width: 300px;}
		ul li{height: 30px;background-color: #eee;color:#666;font-weight:bold;font-size:14px;line-height: 30px;padding:0 20px;list-style:none;}
		ul .side{background-color:#333;color:#fff;}
		ul .focus{font-size:22px;background-color: #555;color:#fff;}
		.near{font-size:18px;background-color: #ccc;color:blue;}
		.sidefocus{background-color: orange;}

	</style>
</head>
<body>
	<ul id="ul">
		<li class="side">这里是首行</li>
		<li>1111</li>
		<li>2222</li>
		<li>3333</li>
		<li>4444</li>
		<li>5555</li>
		<li>6666</li>
		<li>4444</li>
		<li>5555</li>
		<li>6666</li>
		<li>4444</li>
		<li>5555</li>
		<li>6666</li>
		<li>4444</li>
		<li>5555</li>
		<li>6666</li>
		<li>4444</li>
		<li>5555</li>
		<li>6666</li>
		<li class="side">这里是尾行</li>
	</ul>
	<script>
		var ul = document.getElementById("ul");
		var aLis = ul.children;
		var first = ul.firstElementChild;
		var last = ul.lastElementChild;

		for(var i=0;i<aLis.length;i++){
			aLis[i].onmouseover = function(){
				
				
				if(this == first || this == last){
					this.className = "sidefocus";
				}else{
					this.className = "focus";
					this.previousElementSibling.className = "near";
					this.nextElementSibling.className = "near";
					first.className = last.className = "side";

				}
			}

			aLis[i].onmouseout = function(){
				for(var i=0;i<aLis.length;i++){
					aLis[i].className = "";
				}
				first.className = last.className = "side";
			}
		}
```

