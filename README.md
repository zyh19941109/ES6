﻿## ES6
### 面向对象的继承

```
	<!DOCTYPE html>
	<html>
		<head>
			<meta charset="UTF-8">
			<title></title>
		</head>
		<body>
			<script type="text/javascript">
				/*
					 ES6 面向对象的继承
					 super 父类：执行父类的构造函数
					 
				*/
				class User{
					constructor(name,pass){
						this.name = name;
						this.pass = pass;
					}
					showName(){
						alert(this.name)
					}
					showPass(){
						alert(this.pass)
					}
				}
	//			let u1 = new User('zyh',123456)
	//			u1.showName()
	//			u1.showPass()
				
				//继承
				//VipUser扩展自User
				class VipUser extends User{
					constructor(name,pass,level){//子类
						super(name,pass)//父类：执行父类的构造函数
						this.level = level;
					}
					showLevel(){
						alert(this.level)
					}
				}
				let v1 = new VipUser('zyh',123456,1)
				v1.showName()
				v1.showPass()
				v1.showLevel()
			</script>
		</body>
	</html>
```
