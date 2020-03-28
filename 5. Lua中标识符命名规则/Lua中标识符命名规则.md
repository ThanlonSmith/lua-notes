##### 5. Lua中标识符命名规则
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;以字母下划线开头，后面可以使用字母、数字、下划线。最好不要使用下划线加大小字母的标识符，这是为了保证标识符的命名不同于Lua保留字。Lua不使用特殊符号，如@和$以及%等来命名标识符。另外，Lua是一个区分大小写的编程语言。Lua中的关键字有：
| and      | break | do    | else   |
| -------- | ----- | ----- | ------ |
| elseif   | end   | false | for    |
| function | if    | in    | local  |
| nil      | not   | or    | repeat |
| return   | then  | true  | until  |
| while    |       |       |        |
>**`一般约定，首位以下划线开头连接一串大写字母的命名被保留用于Lua的内部全局变量！`**