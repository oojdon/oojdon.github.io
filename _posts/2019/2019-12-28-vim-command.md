---
layout: article
title:  VIM
---

## 历史

```
1976 Bill Joy 发明 VI
1991 Bram Moolenaar 发明 Vim
2015 Thiago de Arruda Padilha 发明  Neovim

```

![](http://cdn.kenblog.top/vim-his.png)


![](/images/vim_cheat_sheet_for_programmers_print.png)

## 启动

```
vim [filename]
```

“可组合性” 使得 Vim 在很大程度上区别于其他编辑器。它赋予了 Vim 独有的语言。


## 模式

```
常规Normal ESC Ctrl+[ 
插入Insert i a o O I A
命令 : 
可视模式Visual v V Ctrl+v
```

## 上下左右

```
k               上移；
j               下移；
h               左移；
l               右移。
```

## 大范围移动

```
ctrl+f      在文件中前移一页（相当于 page down）；
ctrl+b      在文件中后移一页（相当于 page up）；

ctrl+d     半屏
ctrl+u


*         当光标停留在一个单词上，* 键会在文件内搜索该单词，并跳转到下一处；
#         当光标停留在一个单词上，# 在文件内搜索该单词，并跳转到上一处；

gg       将光标定位到文件第一行起始位置；
G        将光标定位到文件最后一行起始位置；
80G      光标移动到第80行


H               将光标移到屏幕上的起始行（或最上行）；
M               将光标移到屏幕中间；
L               将光标移到屏幕最后一行。


zt          把当前行移动到当前屏幕的最上方，也就是第一行
zz          把当前行移动到当前屏幕的中间
zb          把当前行移动到当前屏幕的尾部

)           移动光标到下一个句子。
(           移动光标到上一个句子。

{           段落
}           段落

%   匹配花括号、方括号、括号等。在一个括号的上面，然后按 %，鼠标就会出现在匹配的另外一半括号处。

[[      Jump to function start

[{      Jump to block start

```

## 行内移动

```
w               右移光标到下一个字的开头；
e               右移光标到一个字的末尾；
b               左移光标到前一个字的开头；

0               数字０，左移光标到本行的开始；
$               右移光标，到本行的末尾；

fa              移动到本行下一个为 a 的字符处
;               重复上一行当前搜索
,               反向

^               移动光标，到本行的第一个非空字符。

```

## 删除

```
x                 删除光标所指向的当前字符；
3x                删除光标所指向的前 3 个字符；

dd               删除光标所在行，也是剪切；
cc               剪切当前行并且进入插入模式。

D	             Cut to end of line

d$              从当前光标起删除字符直到行的结束；
d0              从当前光标起删除字符直到行的开始；
J                删除本行的回车符（CR），并和下一行合并。
```

## 复制粘贴

```
yy              复制当前行到内存缓冲区；
nyy             复制 n 行内容到内存缓冲区；
5yy             复制 5 行内容到内存缓冲区；


p               小写字母 p，将缓冲区的内容粘贴到光标的后面；
P               大写字母 P，将缓冲区的内容粘贴到光标的前面。

```

## 撤销和重做

```

u               撤消前一条命令的结果；
.              重复最后一条修改正文的命令。
ctrl + r 恢复撤销操作

```



## 搜索

```
/str1               正向搜索字符串 str1；
n                   继续搜索，找出 str1 字符串下次出现的位置；
N                   继续搜索，找出 str1 字符串上一次出现的位置；
?str2               反向搜索字符串 str2 。
```

## 命令模式

```
:set nu
:set nonu
:n
```

## 可视模式

```

d：剪贴选择的内容到剪贴板。
y：拷贝选择的内容到剪贴板。
c：剪贴选择的内容到剪贴板并且进入插入模式。

```

## 替换

```

rc               用 c 替换光标所指向的当前字符；

s               用输入的正文替换光标所指向的字符；
S               删除当前行，并进入插入模式；

:{作用范围}s/{目标}/{替换}/{替换的标志}

:s/zempty/handsome/g
:%s/zempty/handsome/g
:50,100/old/new/g

```



## 保存退出

```
:q             在未作修改的情况下退出；
:q!               放弃所有修改，退出编辑程序。
:wq
ZZ
:x            退出文件并保存对文件的修改。
```


[参考](http://tnerual.eriogerg.free.fr/vimqrc.html)

[参考](https://github.com/skywind3000/awesome-cheatsheets/blob/master/editors/vim.txt)