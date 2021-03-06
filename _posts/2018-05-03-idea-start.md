---
layout: post
title: "mac 命令"
date: 2018-05-03
category: mac
tags: [mac，idea，命令]
---
#Mac键盘符号和修饰键说明
	⌘ Command
	⇧ Shift
	⌥ Option
	⌃ Control
	↩︎ Return/Enter
	⌫ Delete
	⌦ 向前删除键（Fn+Delete）
	↑ 上箭头
	↓ 下箭头
	← 左箭头
	→ 右箭头
	⇞ Page Up（Fn+↑）
	⇟ Page Down（Fn+↓）
	Home Fn + ←
	End Fn + →
	⇥ 右制表符（Tab键）
	⇤ 左制表符（Shift+Tab）
	⎋ Escape (Esc)

#视图切换
	Comand + 数字 视图区域对应的数字 各视图区域的切换 <!-- more --> 
	Comand + e 列出最近查看的文件列表 
	Shift + Comand + e 最近修改文件列表

#重构
	//Comand+Shift+Alt+T(Refactor This) 整体快捷键 
	//Shift+F6 改名字 
	//Command+F6 可修改参数（实现类的参数能一起修改）

#编辑
```
⌘L  在当前文件跳转到某一行的指定处
⌃Space 基本的代码补全（补全任何类、方法、变量）
⌃⇧Space 智能代码补全（过滤器方法列表和变量的预期类型）
⌘⇧↩ 自动结束代码，行末自动添加分号
⌘P 显示方法的参数信息
⌃J, Mid. button click 快速查看文档
⇧F1 查看外部文档（在某些代码上会触发打开浏览器显示相关文档）
⌘+鼠标放在代码上 显示代码简要信息
⌘F1 在错误或警告处显示具体描述信息
⌘N, ⌃↩, ⌃N 生成代码（getter、setter、构造函数、hashCode/equals,toString）
⌃O 覆盖方法（重写父类方法）
⌃I 实现方法（实现接口中的方法）
⌘⌥T 包围代码（使用if..else, try..catch, for, synchronized等包围选中的代码）
⌘/ 注释/取消注释与行注释
⌘⌥/ 注释/取消注释与块注释
⌥↑ 连续选中代码块
⌥↓ 减少当前选中的代码块
⌃⇧Q 显示上下文信息
⌥↩ 显示意向动作和快速修复代码
⌘⌥L 格式化代码
⌃⌥O 优化import
⌃⌥I 自动缩进线
⇥ / ⇧⇥ 缩进代码 / 反缩进代码
⌘X 剪切当前行或选定的块到剪贴板
⌘C 复制当前行或选定的块到剪贴板
⌘V 从剪贴板粘贴
⌘⇧V 从最近的缓冲区粘贴
⌘D 复制当前行或选定的块
⌘⌫ 删除当前行或选定的块的行
⌃⇧J 智能的将代码拼接成一行
⌘↩ 智能的拆分拼接的行
⇧↩ 开始新的一行
⌘⇧U 大小写切换
⌘⇧] / ⌘⇧[ 选择直到代码块结束/开始
⌥⌦ 删除到单词的末尾（⌦键为Fn+Delete）
⌥⌫ 删除到单词的开头
⌘+ / ⌘- 展开 / 折叠代码块
⌘⇧+ 展开所以代码块
⌘⇧- 折叠所有代码块
⌘W 关闭活动的编辑器选项卡
Command + j 调出快捷 
Command+W 选你所想 
Option+左光标/右光标 可移动到前后的单词 
alt + enter 调出IDEA对出错点的提示处理方法，熟练使用可使你写代码的速度提升5倍 
Command+D 复制黏贴当前行到下一行 
Shift+Command+V 调出最近复制的内容列表 
Command + / 注释/取消注释 
Command + C|V|X 
F2/Shift+F2 跳转到有错误的代码
	
Command+Shift+Enter 
神器，补全当前行，最常用的场景时补全当前行后的；号，并将光标定位到下一行
	
Ctrl+N 
在文件结构上使用，可新建类等。在代码编辑窗口使用，可自动生成getter、setter方法，构造器，重写方法。
	
Command+o 重写方法 
Command + I implement 方法 
Shift + Command + L 格式化代码 
Shift + Command + up/down 将当前代码段上/下移 
Shift + alt + up/down 将当前行上/下移 
大小写转换 Command+Shift+U 
Shift + alt+left/right 返回上次编辑的位置 
Comand+Shift+F9 重新编译文件
```
#查找打开
	Command+Shift+H 查找继承关系
	Command+B： 
	用在类名上–>找到用到该类的类 
	用在方法上–>找到调用该类中的方法
	Command+Alt+B： 
	用在类名上–>找到对应类的实现类 
	用在方法上–>找到实现类中的该方法
	Comand+N 打开类 
	Comand+Shift+N 打开文件 
	在project中，按下ctrl + shift + f(r) 即是在当前目前下递归查找或替换,搜索出来后，要全部替换，按下alt + a 
	Alt+F7 类或方法的使用 
	Comand+F 查找文本出现的位置（F3/Shift+F3前后移动） 
	Comand+R 替换搜索 
	Shift+Shift searchEveryWhere搜索任何东西 
	Comand+F12 查看当前类所有方法 
	Comand+G 跳转到某行 
	Comand+{/} 跳转到光标最近的括号中

#运行程序与debug 
	Crtl+Shift+F10 运行 
	Crtl+Shift+F9 调试 
	Comand+F2 停止 
	F7 单步进入 
	F9 跳过本次debug 
	F8 单步跳过

#其他常用快捷键
	cmd + , 调出setting界面 
	cmd + ; 调出项目setting界面 
	cmd + f4 关闭当前界面