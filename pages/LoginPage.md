---
layout: page
title: 台灣真菌多樣性
subtitle: 公民科學調查
permalink: "LoginPage"
#published: false
#<iframe src="https://ythuangmyco.github.io/fdcs_login/" height="700" width="100%" frameBorder="0"></iframe>
---
<html>
<head>
	<title>An Ajax Web Application</title>
</head>
<body>
<h1 id="page-title"></h1>
<button id="load-data">Click Here to Load the Data</button>
<script>
	document.getElementById("load-data").addEventListener("click",function(){
		var xmlhttp = new XMLHttpRequest();
		xmlhttp.open("GET", "https://ythuangmyco.github.io/fdcs_login/");
		xmlhttp.onreadystatechange = function() {
			document.getElementById("page-title").innerHTML = this.responseText;
		};
		xmlhttp.send();
	});
</script>
</body>
</html>
