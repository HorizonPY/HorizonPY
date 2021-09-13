---
title: C语言的简易弹窗
excerpt: 基于windows.h
tag: 趣味性
date: 2021-9-13
categories: 
- 编程娱乐向
---

### 利用C语言中 Windows.h 中的 MessageBox 实现简易弹窗

#### MessageBox 基本形式
```
    MessageBox(HWND hWnd,LPCTSTR lpText,LPCTSTR lpCaption,UINT UType);
```
说人话就是
```
    MessageBox(句柄, 显示内容,标题,按钮);
```
句柄是什么？
目前完全可以忽略掉~

关于按钮类型有几种常见的：
MB_ABORTRETRYIGNORE
MB_OKCANCEL
MB_RETRYCANCEL
MB_YESNO
MB_YESNOCANCEL
MB_OK

这里就不介绍对应的按钮实际是怎样的，试一试就知道了

#### 示例#1
```
    MessageBox(NULL,"hello","test",MB_OK);
```

<img src="/img/13-1.png" width="25%" height="25%">

#### 示例#2

如果加上循环的话就可以无限的弹出
```
while(1)
	MessageBox(NULL,"hello","test",MB_OK);
```

### 结尾
使用 Windows.h 内的 MessageBox 可以实现简单的 Windows 弹窗，更复杂的类似于 句柄 的相关概念可以继续深入了解，本文章仅作介绍，不赘述~