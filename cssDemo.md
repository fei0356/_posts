---
title: 一些不常用的css
date: 2017-01-04 10:25:15
tags:
---

## table自动合并边框

	table{
		border-collapse: collapse;
	}
##  div文本超出隐藏＋...
###### 单行隐藏
	overflow:hidden; //超出的文本隐藏

	text-overflow:ellipsis; //溢出用省略号显示

	white-space:nowrap; //溢出不换行
###### 多行隐藏
	display:-webkit-box; //将对象作为弹性伸缩盒子模型显示。

	-webkit-box-orient:vertical; //从上到下垂直排列子元素（设置伸缩盒子的子元素排列方式）

	-webkit-line-clamp:2; //这个属性不是css的规范属性，需要组合上面两个属性，表示显示的行数。
	
	
## 计算属性
	width: calc(100%/3 - 5px) //兼容性良好