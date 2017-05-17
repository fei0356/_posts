---
title: 常见js排序算法
date: 2017-05-17 15:18:50
tags:
---

        console.log("冒泡");
    	var arr = [1,24,4,2,67,2124,43,2]
		var bubbleSort = function(arr){
			if(arr.length <= 1){
				return arr
			}
			var temp;
			for(var i = 0; i < arr.length-1 ;i++){
				for(var j = i+1; j<arr.length; j++){
					if(arr[i] > arr[j]){
						temp = arr[i];
						arr[i] = arr[j];
						arr[j] = temp;
					}
				}
			}
			return console.log(arr);
		}
		bubbleSort(arr);
		
		console.log("快速")
		var quickSort = function(arr){
			if(arr.length <= 1){
				return arr
			};
			var left = [];
			var right = [];
			var pointIndex = Math.floor(arr.length/2);
			var point = arr.splice(pointIndex,1)[0];
			for (var i = 0; i < arr.length; i++) {
				if (arr[i] < point) {
					left.push(arr[i])
				}else {
					right.push(arr[i])
				}
			}
			return quickSort(left).concat([point],quickSort(right));
			
		}
		console.log(quickSort(arr))
		
		console.log("选择")
		var selectSort = function(arr){
			var index, min, temp;
			for (var i = 0; i < arr.length; i++) {
				index = i;
				min = arr[i];
				for (var j = i + 1; j < arr.length; j++) {
					if (arr[j] < min){
						index = j;
					}
				}
				if(index != i){
					temp = arr[i];
					arr[i] = arr[index];
					arr[index] = temp;	
				}
			}
			return arr
		}
		console.log(selectSort([1,24,4,2,67,2124,43,2]));
		
		console.log("插入排序");
		var insert = function(arr){
			var index,insert;
			for(var i = 0; i<arr.length-1 ;i++){
				index = i + 1;
				insert = arr[i+1];
				for(var j = i; j >= 0 ;j--){
					if(arr[j] > insert){
						arr[j+1] = arr[j]
						index = j;
					}
				}
				arr[index] = insert;
			}
			return arr
		}
		console.log(insert([1,24,4,2,67,2124,43,2]))