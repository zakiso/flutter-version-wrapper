### Flutter version wrapper

flutterw: Solve gadgets with inconsistent versions when multiple people develop flutter projects at the same time. Inspired by gradlew.

**work on macOS & Linux**

### Instructions for use
1. Execute the command to download the script in your project root directory
`curl -O https://raw.githubusercontent.com/zakiso/flutterw/master/flutterw && chmod 755 flutterw`

2. Download the script and use it in the root directory
`./flutterw init`
This command will collect the flutter version in your current system and write the relevant information into the `flutter_wrapper.properties` file. All members of the team will use this version number as the standard version of the project

3. Add the flutterw file and flutter_wrapper.properties file to git and submit to the warehouse

4. After other members pull the code and use the `flutter` command in the project, use `./flutterw` instead


### What did flutterw do?
1. When using flutterw, it will get the version number in the flutter_wrapper.properties file in the current directory
2. Go to the user's `${HOME}/flutter_wrapper/{version number}/` directory to find if there is this version of the SDK
3. If there is no version of the SDK, it will be downloaded, and then use the SDK in this directory to execute the command


### Flutter version wrapper

flutterw：解决多人同时开发flutter项目的时候，版本不一致的小工具。灵感来源于gradlew。

**work on macOS & Linux**

### 使用说明
1. 在你的项目根目录中执行命令下载脚本   
`curl -O https://raw.githubusercontent.com/zakiso/flutterw/master/flutterw && chmod 755 flutterw`

2. 下载好脚本后在根目录中使用  
`./flutterw init`  
该命令会收集你当前系统中的flutter版本，并将相关信息写入`flutter_wrapper.properties`文件中，团队中所有成员都会以该版本号做为该项目的标准版本  

3. 将flutterw文件和flutter_wrapper.properties文件添加到git中提交到仓库里

4. 其他成员拉取代码后在项目中使用`flutter`命令的地方使用`./flutterw`代替


### flutterw做了什么？
1. 使用flutterw的时候会获取当前目录下的flutter_wrapper.properties文件中的版本号
2. 去用户的`${HOME}/flutter_wrapper/{版本号}/` 目录下查找是否有该版本sdk
3. 如果没有该版本sdk会下载下来，然后使用该目录下的sdk执行命令
