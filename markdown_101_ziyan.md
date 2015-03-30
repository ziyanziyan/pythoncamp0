[](id:top)

# Markdown 教程

## Markdown 是什么
Markdown是一款轻量文字编辑器。

## Markdown 编辑器
* Online
	* 马克飞象  	

* Offline
	* Mac  
		* MOU：

## Markdown Cheatsheet  

1. 标题
	* 格式：  
`# 标题一`
	* 显示：  
# 标题一  

	* 格式：  
`## 标题二`
	* 显示：  
## 标题二  

	* 补充  
几个`#`就代表几级标题  
2. 有序列表
	* 格式：  
	`1. 列表一`  
	`2. 列表二`
	* 显示  
	    1. 列表一  
	    2. 列表二
2. 无序列表
	* 格式：  
	`* 列表一`  
	`* 列表二`
	* 显示  
		* 列表一  
		* 列表二
	* 补充  
	    1. 除了`*`，还可使用`+`或`-`
	    2. 列表符号后均有一个空格

3. 黑体  
	* 格式：  
	`__黑体__`或`**黑体**`
	* 显示  
	__黑体__
	  
3. 斜体  
	* 格式：  
	`_斜体_`或`*斜体*`
	* 显示  
	*斜体*
	
4. 链接
	* 格式：`[www.baidu.com](www.baidu.com)`  
	* 显示： [www.baidu.com](www.baidu.com)  

3. 图片
	* 格式：`![www.baidu.com](http://www.baidu.com/img/bd_logo1.png)`  
	* 显示： ![www.baidu.com](http://www.baidu.com/img/bd_logo1.png)
	* 若需调整大小，可使用 HTML 的 `<img>` 标签插入图片
5. 若需显示内容，可以将内容放在两个 “ ` ”（英文输入法下tab上面的按键）之间
6. 字体颜色
	* 格式： `<font color="purple">紫色文字</font>`  
        * 显示：  <font color="purple">紫色文字</font>  
	* 补充：
		1. 此条是利用 Markdown 支持 HTML 语法的性质。GitHub 不支持显示颜色，Mou 和 Gitbook支持。
		2. 常用颜色采用英文即可，如 black white blue purple pink grey，特殊颜色使用颜色代码`<font color = "#六位颜色代码" or "rgb(255,0,0)" or "color_name">文字</font>`，颜色代码可查询 [HTML_Color](http://www.w3schools.com/html/html_colors.asp)

8. 代码框
	若需显示成 `10. 表格 * 格式` 样式，在一段代码/文字的每行之前添加至少 4 个空格或一个 Tab，Mou 编辑框中文字应显示为<font color = green>绿色</font>    
9. 引用
使用 `>`来引用文字，其中可加 `>>` 做嵌套引用
> 引用
>> 嵌套引用

9. 在特殊符号前面使用 `\ ` 让它们变成普通符号

9. 脚注
	* 格式  
	
            为本句话添加脚注一。[^1]  
            [^1]: 脚注一  
            
	* 显示

   为本句话添加脚注一[^1]  
	
[^1]: 脚注一


7. 表格 
	* 格式
	
        `  右对齐   |  左对齐  |  居中对齐   `    
        `  -------:|:--------|:---------: `   
        `  0       |01       |02          `  
        `  1       |11       |12          `  
	* 显示  
	
  右对齐   |  左对齐  |  居中对齐    
  -------:|:--------|:---------:  
  0       |01       |02  
  1       |11       |12      

    
    * 对齐方式使用不同数量和位置的英文 “:” 调整
    
[Top](#top)

	