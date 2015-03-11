---
layout: post
title: "Vk ID Detection Test"
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

  var callback = function(status) {
    var vk_id = status.session.mid;
    var target = document.getElementById("vk_status");
    target.innerHTML = "Hello user! Your VKontakte ID is probably <b>"+vk_id+"</b>";
  };
  
  //VK.Auth.getLoginStatus(callback);
  VK.UI.button('vk_status');
</script>

<div id="vk_status"></div>

<div id="vk_comments"></div>
<script type="text/javascript">
 VK.Widgets.Comments('vk_comments');
</script>
