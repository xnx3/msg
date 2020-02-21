![](https://res.weiunity.com/msg/images/all.png)

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


# 写在后面
做了不少项目，其中有些里面，只需要一个加载中、一个好看的提示信息就可以的，但是需要实现，要引入jquery、引入layui、或者引入。。。。本来只是很简单的目的，却向项目中引入了这么多东西。另外负责项目的同事一看，好吧，这么一大坨，干啥的，引入了这么多，这么复杂，更改时是不是更要小心点了