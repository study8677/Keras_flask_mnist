# Keras_flask_mnist
基于 TensorFlow2.0 （Keras） + Flask 的 Mnist 手写数字集识别系统

### 更新记录
- 2020-03-17 使用redis实现记录访问次数的功能
- 2020-04-25 增加 判断访问次数是否异常，如异常则从日志中读取。（最近有人使用我的线上redis进行线下调试，以及一些其他原因导致会重置访问次数，增加下判断）
- 2020-05-01 增加 了 redis 服务异常 短信通知，当然只有在我的服务器上才能用
- 2020-05-10 redis增加了访问密码
- 2020-06-10 增加了vue前后端分离（Vue）

- 演示地址
```
http://101.42.235.106:8835/ （公网IP访问）
http://paulson.free.idcfengye.com/ （内网穿透 ngrox 域名访问） 可以看下面我的博客链接地址  # 暂不支持
http://http://101.42.235.106:8836   （前后端分离 vue版访问路径--原服务器下掉了，新的服务还没部署）
```

- 下载

**新手部署使用注意**
注释掉 app.py 中 使用 redis 记录访问次数的功能
主要是这个方法的使用与引用
get_visit_info()


### 部署
- 下载
```c
git clone https://github.com/ybsdegit/Keras_flask_mnist.git
```
- 安装依赖
```
pip install -r requirements.txt
```

# 运行

- 启动服务
```
python app.py
```
本地启动访问地址为：`http://localhost:3335/`

- 训练
源码中也包含训练好的模型 `model.h5`,测试集成功率99.9，也可以自行训练。
```
python model/train.py
```


### 博客
```
https://blog.csdn.net/qq_38534107/article/details/103565899 （mnist）
https://blog.csdn.net/qq_38534107/article/details/106009215 （内网穿透）
```


### 声明 （2019年12月16日晚23点）
识别率达到95%以上。已经是个成熟的demo了

求star
