---
layout: post
title: "Vk Comments"
description: ""
category: 
tags: []
---
{% include JB/setup %}

<script src="//vk.com/js/api/openapi.js" type="text/javascript" charset="windows-1251"></script>
<script type="text/javascript">
  VK.init({
    apiId: 4822267,
    onlyWidgets: true
  });

  vk_id = null;

  var callback = function(status) {
    var vk_id = status.session.mid;
    var target = document.getElementById("vk_comments");
    target.innerHTML = "Hello user! Your VKontakte ID is probably <b>"+vk_id+"</b>";
  };
  
  VK.Auth.getLoginStatus(callback);
</script>

<div id="vk_comments"></div>
