---
title: 获取url参数
date: 2017-05-25 13:33:50
tags:
---


getHref: function(){
    var href = location.href
    //		var href = 'http://www.test.qdd.xyz:8080?id=1'
    var s = href.split('?')[1].split('&');
    var d = {};
    $.each(s,function(index,item){
        d[item.split('=')[0]] = item.split('=')[1]
    })
    return d
}
