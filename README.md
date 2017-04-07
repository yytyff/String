###5、写一个函数，判断一个字符串是回文字符串，如 abcdcba是回文字符串, abcdcbb不是
```
var a = 'abcdcba';
var b = 'abcdcbb';
function isReverse(str){
	return str ===str.split('').reverse().join('');
}
console.log (isReverse(a));
console.log (isReverse(b));
```
###6、写一个函数，统计字符串里出现出现频率最多的字符
```
var str ='hello world , jiengu haha hoho hoho lol'
var dict = {}
for (var i = 0; i < str.length; i++) {
	if(dict[str[i]]) {
		++dict[str[i]]
	}else{
		dict[str[i]] = 1
	}
}
var count= 0
var maxValue
for(key in dict){
	if(dict[key] > count){
		maxValue = key
		count = dict[key]
	}
}
console.log(maxValue,count)
```
###7、写一个camelize函数，把my-short-string形式的字符串转化成myShortString形式的字符串，如
```
function camelize(str){
	var arr = str.split('-');
	var newArr = arr[0];
	for (var i = 1; i < arr.length; i++) {
		newArr += arr[i].charAt(0).toUpperCase() 
		+ arr[i].slice(1,arr[i].length);
	}
	return newArr;
}	

console.log(camelize("background-color"));
console.log(camelize("list-style-image"));

camelize("background-color") == 'backgroundColor'
camelize("list-style-image") == 'listStyleImage'
```
###8、写一个 ucFirst函数，返回第一个字母为大写的字符 （***）
```
var str= 'hello';
function ucFirst(str){
	
	var str1 = str.charAt(0).toUpperCase();
 	var str2 = str.slice(1);
 	return str1 + str2;
}

ucFirst(str);

ucFirst("hunger") == "Hunger"
```
###9、写一个函数truncate(str, maxlength), 如果str的长度大于maxlength，会把str截断到maxlength长，并加上...，如
```
function truncate(str,maxLength){
	var strLength = str.length;
	var newStr;
	if(str.length > maxLength){
		newStr = str.slice(0,maxLength) + "...";
	} else{
		newStr = str;
	}
	return newStr;
}

truncate("hello, this is hunger valley,", 10)) == "hello, thi...";
truncate("hello world", 20)) == "hello world"
```
