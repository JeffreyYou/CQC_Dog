## Showing LaTeX formulas in GitHub 数学公式

### 1. 插入数学公式的方法

#### 方法1

So the solution would be to insert this code in Markdown files:

```html
<div align=center><img src="https://render.githubusercontent.com/render/math?math=e^{i \pi} = -1"></div>
```

```
\large \Large \LARGE \huge \Huge 改变公式大小
```

Example：

<img src="https://render.githubusercontent.com/render/math?math=\Huge e^{i \pi} = -1">

#### 方法2

```html
<div align=center><img src="http://chart.googleapis.com/chart?cht=tx&chl= \frac{N_n(O_i)}{n}"></div>
```

Example:

<img src="http://chart.googleapis.com/chart?cht=tx&chl=\Huge \frac{N_n(O_i)}{n}">

### 2. 公式居中（图片）



```html
<img align="left" width="100" height="100" src="http://www.fillmurray.com/100/100">
```

```html
<p align="center">
  <img width="460" height="300" src="http://www.fillmurray.com/460/300">
</p>
```

```html
<img align="right" width="100" height="100" src="http://www.fillmurray.com/100/100">
```

<p align="center">
  <img width="460" height="300" src="http://www.fillmurray.com/460/300">
</p>


### 3. 特殊符号

`+` symbol is used to escape spaces in [URI encoding](https://en.wikipedia.org/wiki/Percent-encoding) and the formula has to be either properly escaped or at least don't conflict with possible escaped version created by the browser. The browser replaces spaces by `+` or `%20` before sending to the server, so when it encounters `+` it assumes that it is already escaped and sends `+` sign as is, which is decoded by the server as a space. So `+` should be replaced by encoded version, which is `%2B`.

To be short: a formula with pluses should be written like this

```html
<img src="https://render.githubusercontent.com/render/math?math=e^{i %2B\pi} =x%2B1">
```

To encode other symbols or entire formulas you can use [`encodeURIComponent`](https://developer.mozilla.org/en/docs/Web/JavaScript/Reference/Global_Objects/encodeURIComponent) function from you browser's developer console.





### Math style显示格式

[Display style in math mode](https://www.overleaf.com/learn/latex/Display_style_in_math_mode)



### 资料来源

1. [Showing LaTeX formulas in GitHub](https://gist.github.com/a-rodin/fef3f543412d6e1ec5b6cf55bf197d7b)
2. [Stack Over Flow: How to show math equations in general github's markdown](https://stackoverflow.com/questions/11256433/how-to-show-math-equations-in-general-githubs-markdownnot-githubs-blog)
3. [Latex Syntax](https://www.overleaf.com/learn/latex/Mathematical_expressions)

