# Markdown Cheat Sheet





## 1. Text Composition 文字排版

### (a) Title 标题排版

用1个#表示总标题

用2个##表示大标题，数字1,2,3表示顺序

用3个###表示每个知识点标题，字母a,b,c表示顺序

用4个####表示每个子标题标题，希腊字母i,ii,iii表示顺序

### (b) Table of Content 生成目录

用Vscode打开对应的Markdown文件

下载插件 `Markdown All in one`

打开控制台 `Ctrl + Shift + P`

使用 `Create Table of Content`

### (c) 目录模板

[Directory Cheat Sheet and Sample](./Directory.md)

### (d) Center Table 居中表格

```html
<table align=center style='text-align:center;' >  
    <tr>    
        <th></th>    
        <th>Binary Heap</th>    
        <th>Binominal Heap</th>
    </tr>
    <tr>    
        <td >Find-Min</td>    
        <td >O( 1 )</td>    
        <td >O( Log(n) )</td> 
    </tr>
    <tr>    
        <td>Insert</td>    
        <td>O( Log(n) )</td>    
        <td>O( Log(n) )</td>  
    </tr>
</table>
```

此方法无法使表内文字居中





## 2. Special Effect 特效渲染

### (a) Picture 插入图片

```html
<div align=center><img width="800"  src="./Pictures/3.PNG"/></div>
```

在GitHub中的图片都是居中显示的

### (b) Emoji 插入表情

[GitHub Emoji Cheat Sheet](./Emoji.md)

### (c) Math 插入数学公式

[GitHub Math Cheat Sheet](./Math.md)