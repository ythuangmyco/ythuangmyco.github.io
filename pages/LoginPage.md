---
layout: page
title: 台灣真菌多樣性
subtitle: 公民科學調查
permalink: "LoginPage"
#published: false
#<iframe src="https://ythuangmyco.github.io/fdcs_login/" height="700" width="100%" frameBorder="0"></iframe>
---
$.ajax({
    url: "https://ythuangmyco.github.io/fdcs_login/",
    data: { uname: "test" },
    type: "GET",
    beforeSend: function(xhr){xhr.setRequestHeader('X-TOKEN', 'xxxxx');},
    success: function() { alert('Success!' + authHeader); }
});

