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
<h1>The XMLHttpRequest Object</h1>
<button type="button" onclick="loadDoc()">Change Content</button>
</div>

<script>
function loadDoc() {
  var xhttp = new XMLHttpRequest();
  xhttp.onreadystatechange = function() {
    if (this.readyState == 4 && this.status == 200) {
      document.getElementById("demo").innerHTML =
      this.responseText;
    }
  };
  xhttp.open("GET", "https://ythuangmyco.github.io/fdcs_login/", true);
  xhttp.send();
}
</script>

</body>
</html>
