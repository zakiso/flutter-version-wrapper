### Flutter version wrapper

flutterw：解决多人同时开发flutter项目的时候，版本不一致的小工具。灵感来源于gradlew。

**only test on mac**

### 使用说明
1. 在你的项目根目录中执行命令下载脚本   
`curl -O https://raw.githubusercontent.com/zakiso/flutterw/master/flutterw`

2. 下载好脚本后在根目录中使用  
`flutterw init`  
该命令会收集你当前系统中的flutter版本，并将相关信息写入`flutter_wrapper.properties`文件中，团队中所有成员都会以该版本号做为该项目的标准版本  

3. 将flutterw文件和flutter_wrapper.properties文件添加到git中提交到仓库里

4. 其他成员拉取代码后在项目中使用`flutter`命令的地方使用`flutterw`代替


### flutterw做了什么？
1. 使用flutterw的时候会获取当前目录下的flutter_wrapper.properties文件中的版本号
2. 去用户的home目录的./flutter_wrapper/{版本号}/ 目录下查找是否有该版本sdk
3. 如果没有该版本sdk会下载下来，然后使用该目录下的sdk执行命令