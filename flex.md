---
title: flex布局（常用属性）
date: 2017-02-23 11:43:37
tags:
---
## flex 布局

	父容器{
		flex-direction
		flex-wrap
		flex-flow
		justify-content
		align-items
		align-content
	}
	子容器{
		order
		flex-grow
		flex-shrink
		flex-basis
		flex
		align-self
	}
	
## demo 圣杯响应式布局

	<!DOCTYPE html>
	<html>
	<head>
		<meta charset="UTF-8">
		<title></title>
	</head>
	<style>
	*{
		margin:0;
		padding:0;
	}
	html,body{
		width:100%;
		height:100%;
	}
	body{
		display: flex;
		flex-flow: column;
	}
	header,footer{
		border:1px solid red;
		flex: 1;
		height:10px;
	}
	
	footer{
		
	}
	.box{
		display: flex;
		flex:4;
	}
	.slide,.ad{
		flex:0 0 50px;
		border:1px solid blue;
	}
	
	.content{
		border:1px solid blue;
		flex:auto;
	}
	.slide{
		order:-1;
	}
	@media only screen and (max-width:768px ) {
		.slide,.ad{
			flex:auto;
			border:1px solid blue;
		}
		.box{
			flex-flow: column;
		}
	}
	</style>
	<body>
		<header></header>
		
		<div class="box">
			<div class="content"></div>
			<div class="slide"></div>
			
			<div class="ad"></div>
		</div>
		
		<footer></footer>
	</body>
	</html>
