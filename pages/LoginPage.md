---
layout: page
title: 台灣真菌多樣性
subtitle: 公民科學調查
permalink: "LoginPage"
#published: false
#<iframe src="https://ythuangmyco.github.io/fdcs_login/" height="700" width="100%" frameBorder="0"></iframe>
---
<!DOCTYPE html>
<html>
<body>

<div id="demo">
  <h2>Let AJAX change this text</h2>
  <button type="button" onclick="loadDoc()">Change Content</button>
</div>

</body>
</html>

function loadDoc() {
  var xhttp = new XMLHttpRequest();
  xhttp.onreadystatechange = function() {
    if (this.readyState == 4 && this.status == 200) {
     document.getElementById("demo").innerHTML = https://ythuangmyco.github.io/fdcs_login/;
    }
  };
  xhttp.open("GET", "ajax_info.txt", true);
  xhttp.send();
}
