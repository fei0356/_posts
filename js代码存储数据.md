---
title: js代码存储数据
date: 2017-05-17 15:07:47
tags:
---


    var Data = {

        set: function(n, v) {
            Data.data[n] = v;
            return true;
        },

        data: {},

        get: function(n) {
            return Data.data[n];
        }
    };
