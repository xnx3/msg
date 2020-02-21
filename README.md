# msg
加载中、成功提示、失败提示等。Loading, success prompt, failure prompt, etc

![](https://res.weiunity.com/msg/images/all.png)

# 快速使用
### 第一步，引入 msg.js 
<script src="./msg.js"></script>
### 第二步，一行代码使用
1. msg.info('Hello Msg')
信息提示，2.5秒后自动关闭

1. msg.success('操作成功')
成功提示，1.5秒后自动关闭

1. msg.failure('操作失败');
失败提示，2.5秒后自动关闭

1. msg.loading('加载中');
加载中的提示，图片会有一张动图一直转圈。不会自动关闭，配合 msg.close(); 一起使用

1. msg.close();
主要用来配合 msg.loading(); 来使用，关闭加载中的提示。
其他的 msg.info()、 msg.success()、 msg.failure() 这些也可以用此来进行关闭，只不过实际使用时，没什么必要

![](http://res.weiunity.com/msg/images/success.png)

> msg.failure('操作失败')

![](http://res.weiunity.com/msg/images/failure.png)

> msg.loading('加载中')

![](http://res.weiunity.com/msg/images/loading.gif)

> msg.close()