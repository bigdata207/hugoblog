```
<!DOCTYPE html>
<html>
<head> 
<meta charset="utf-8"> 
<title>菜鸟教程(runoob.com)</title> 
</head>
<body>

<p id="h">创建和使用对象方法。</p>
<p id="p">对象方法作为一个函数定义存储在对象属性中。</p>
<p id="demo"></p>
<script>
	function fullName(person){
		alert(person.firstName)
		return person.firstName + "<br>" + person.lastName;
	}
</script>
	
<script>
var person = {
    firstName: document.getElementById("h").innerHTML,
    lastName : document.getElementById("p").innerHTML,
    id : 5566,
    fullName : function(){
		return fullName(this)
	}
};
document.getElementById("demo").innerHTML = person.fullName();
</script>

</body>
</html>
```

对象属性可根据外部html标签值改变，而对象内的函数也可以复用外部函数，多一层调用
