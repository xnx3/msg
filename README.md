![](https://res.weiunity.com/msg/images/all.png)

## 快速体验
http://res.weiunity.com/msg/demo.html

# 快速使用
### 第一步，引入 msg.js 
<script src="https://res.weiunity.com/msg/msg.js"></script>
### 第二步，一行代码使用
````
msg.info('Hello Msg')
````
信息提示，2.5秒后自动关闭

````
msg.success('操作成功')
````
成功提示，1.5秒后自动关闭

````
msg.failure('操作失败');
````
失败提示，2.5秒后自动关闭

````
msg.loading('加载中');
````
加载中的提示，图片会有一张动图一直转圈。不会自动关闭，配合 msg.close(); 一起使用

````
msg.close();
````
主要用来配合 msg.loading(); 来使用，关闭加载中的提示。
其他的 msg.info()、 msg.success()、 msg.failure() 这些也可以用此来进行关闭，只不过实际使用时，没什么必要

### 弹出提示，提示消失时执行其他命令
弹出提醒，提醒消失时，弹出alert提示框的代码示例：
````
msg.info('Hello Msg', function(){
	alert(123);
});
````
msg.info() 、 msg.success()、 msg.failure() 这三个都支持这种方式。

### 弹出层
````
//普通弹出框。普通弹出窗只是显示内容，所以直接吧内容传入就可以了
msg.popups('我是弹出窗口，可以传入文字、也可以传入html');

//自定义弹出框。自定义，传入了一个自定义属性，内容文本也算是其中的一个属性。
msg.popups({
	text:'弹窗的内容',	//弹出窗显示的内容，支持html
	top:'30%',			//弹出层距离顶部的距离，不传默认是30%。 可以传入如 30%、 5rem、 10px 等
	left:'5%',			//弹出层距离浏览器左侧的距离，不传默认是5%
	height:'100px',		//弹出层显示的高度。不传默认是 auto。 传入如 100px 、 10rem 等 
	width:'90%',		//弹出层显示的宽度。不传默认是 90%
	bottom:'1rem',		//弹出层距离底部的距离。不传默认是 auto 。 height 跟 bottom 如果这两个同时设置了，那么height生效，bottom是不生效的
	close:false			//是否显示右上角的关闭按钮，不传默认是true，显示关闭按钮
	background:'#2e2d3c'	//背景颜色。十六进制颜色编码。不传默认是 '#2e2d3c'
	opacity:92			//弹出层的透明度，默认是92, 取值0~100，0是不透明，100是全部透明
});
````

# 写在后面
做了不少项目，其中有些里面，只需要一个加载中、一个好看的提示信息就可以的，但是需要实现，要引入jquery、引入layui、或者引入。。。。本来只是很简单的目的，却向项目中引入了这么多东西。另外负责项目的同事一看，好吧，这么一大坨，干啥的，引入了这么多，这么复杂，更改时是不是更要小心点了。

msg.js已在 网市场云建站系统 https://gitee.com/mail_osc/wangmarket 等项目中采用。