##### di2. Lua环境的安装
Linux平台[以Ubuntu Linux系统为例]：
```py
# 从官网下载lua安装包，下载地址是http://www.lua.org/ftp/lua-5.3.5.tar.gz
thanlon@thanlon-master:/usr/local$ curl -R -O http://www.lua.org/ftp/lua-5.3.5.tar.gz
# 解压安装包
thanlon@thanlon-master:/usr/local$ tar zxvf lua-5.3.5.tar.gz
# 进入安装包
thanlon@thanlon-master:/usr/local$ cd lua-5.3.5/
# 编译
thanlon@thanlon-master:/usr/local$ sudo make linux test
# 安装
thanlon@thanlon-master:/usr/local$ sudo make linux install
```
>**`遇到以下问题的原因是缺少相关库：`**
>```py
>lua.c:82:10: fatal error: readline/readline.h: 没有那个文件或目录
>82 | #include <readline/readline.h>
>      |                    ^~~~~~~~~~~~~~~~~~~~~
>compilation terminated.
>make[2]: *** [<内置>：lua.o] 错误 1
>make[2]: 离开目录“/usr/local/lua-5.3.5/src”
>make[1]: *** [Makefile:110：linux] 错误 2
>make[1]: 离开目录“/usr/local/lua-5.3.5/src”
>make: *** [Makefile:55：linux] 错误 2
>```
>**`以上问题的解决方式是安装缺失的库：`**
>```py
># 安装libreadline-dev库，然后再重新编译、安装
>sudo apt install libreadline-dev
>```

安装集成开发环境 [**ZeroBrane Studio**](https://studio.zerobrane.com/download?not-this-time)：
```py
# 下载ZeroBrane Studio安装脚本(shell)，注意安装的过程中可能比较慢，需要科学上网工具的帮助
thanlon@thanlon-master:/usr/local$ wget https://download.zerobrane.com/ZeroBraneStudioEduPack-1.90-linux.sh
# 给这个shell脚本执行的权限
thanlon@thanlon-master:/usr/local$ chmod +x ZeroBraneStudioEduPack-1.90-linux.sh
# 执行这个脚本后，ZeroBrane Studio就会被安装
thanlon@thanlon-master:/usr/local$ ./ZeroBraneStudioEduPack-1.90-linux.sh
# 安装成功后，执行zbstudio命令可以打开ZeroBrane Studio
thanlon@thanlon-master:/usr/local$ zbstudio
# 执行zbstudio-uninstall命令可以卸载ZeroBrane Studio
thanlon@thanlon-master:/usr/local$ zbstudio-uninstall
```
Windows平台：

可以直接下载安装 [**LuaForWindows_v5.1.5-52.exe**](https://github.com/rjpcomputing/luaforwindows/releases/download/v5.1.5-52/LuaForWindows_v5.1.5-52.exe)，里面包含了Lua环境和集成开发环境SciTE。当然 Windows平台下也可以使用ZeroBrane Studio，下载页面 [**https://studio.zerobrane.com/download**](https://studio.zerobrane.com/download)。安装不比Linux平台困难，这里不再做详细介绍。