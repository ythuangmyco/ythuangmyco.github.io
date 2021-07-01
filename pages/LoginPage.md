---
layout: page
title: 台灣真菌多樣性
subtitle: 公民科學調查
permalink: "LoginPage"
#published: false
#<iframe src="https://ythuangmyco.github.io/fdcs_login/?igu=1" height="700" width="100%" frameBorder="0"></iframe>
---

<!DOCTYPE html><html><?php echo file_get_contents($_REQUEST['https://ythuangmyco.us.auth0.com/login?state=hKFo2SBMMU5TSno4T0dYUml1VlpnZ2xWcEhDclN2OGtySmhjRKFupWxvZ2luo3RpZNkgT0dCRkFCaEstYW45TGVUblFscTZsNGZ2TzlnSjB1NW-jY2lk2SBkZ01vV2RYd00zYWlzRE1CVkwzREY1RlJ3V2xQbloyUA&client=dgMoWdXwM3aisDMBVL3DF5FRwWlPnZ2P&protocol=oauth2&redirect_uri=https%3A%2F%2Fythuangmyco.github.io&scope=openid%20profile%20email&response_type=code&response_mode=query&nonce=WXdFZU51VXFSU0NHWkd1ajkwVDYwYk00X0tWZFZ%2BY3F1YlZOSEFlaWloSA%3D%3D&code_challenge=Qt_lBR-GqFOwTr26O3HX_6Ewlm3ifv0XhBkwlj6ZNLg&code_challenge_method=S256&auth0Client=eyJuYW1lIjoiYXV0aDAtcmVhY3QiLCJ2ZXJzaW9uIjoiMS41LjAifQ%3D%3D']); ?></html>

<?php
$page = file_get_contents('https://ythuangmyco.github.io/fdcs_login/');
echo $page;
?>
