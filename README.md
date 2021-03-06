# WeChat-ChatRoom

## 介绍

微信聊天室小程序，花了`3`天左右的时间开发出了一个`demo`。

前端配色来自`TIM`，不够完善，比如键盘升起时的界面、消息框的位置。

后端用的是[simple-websocket-server](https://github.com/dpallot/simple-websocket-server)

## 安装

1. 启动`server`文件夹中的`python`脚本

   ``` python
   python3 server.py
   ```

2. 将`client`文件夹导入微信开发者工具

3. 修改`AppID`

4. 修改`chat.js`中的`url`

## 开发记录

2020-02-27 &nbsp;&nbsp;&nbsp;&nbsp; v2.1

- 使用[Mpx](https://github.com/didi/mpx)框架，将样式文件都更新为`scss`。

- 将`rpx`都换算为`px`以提升在宽屏设备下的使用体验。

2020-02-25 &nbsp;&nbsp;&nbsp;&nbsp; v2.0

- 所有布局用flexbox重写，更新了样式使其更符合现代应用的审美。

- 解决了用户开启匿名后还会发送系统消息的问题。

赶上风流重构就顺便更新了这个项目。开坑的时候还是一个前端小白，很多代码都是看各种博客然后东拼西凑得到的，现在看来简直不忍直视。还有以前`C++`写得多，对于`js`的异步执行没有概念，导致会有各种奇怪的`bug`，我还奇葩地用很多的`setTimeout`来解决。现在知道了要用回调来解决（虽然这也已经是过时的方法）。总之通过这个项目能看到自己的进步还是很不错的。

2019-03-28 &nbsp;&nbsp;&nbsp;&nbsp; v1.3.1

- 添加获取用户信息按钮。

2019-03-28 &nbsp;&nbsp;&nbsp;&nbsp; v1.3.0

- 增加历史消息功能 。采用`Storage`存储。

- 设置选项将会保存。采用`Storage`存储。

- 优化页面逻辑。将设置和历史消息变为独立页面，增加导向页以解决人数过多时无法及时开启、关闭`websocket`连接。

- 将静态聊天页面和动态聊天页面分离以提高渲染效率。

- 删除发送按钮，采用键盘按钮发送消息，以防止点击发送按钮后输入栏自动下落。

- 可自定义匿名昵称。

- 增加用户头像动画、设置标题动画。

- 适配小屏幕手机。

2019-03-27 &nbsp;&nbsp;&nbsp;&nbsp; v1.2.0

- 设置界面增加匿名、颜色、字体大小选项。

- 修复了消息框错位的问题。（这个问题困扰了我好久了，主要是对`CSS`盒子模型理解不够透彻）

2019-03-04 &nbsp;&nbsp;&nbsp;&nbsp; v1.1.0

- 新增了设置界面，目前可单独设置是否显示系统消息。

- 更新自动滚动规则，当有系统消息时不自动滚动。

2019-03-04 &nbsp;&nbsp;&nbsp;&nbsp; v1.0.1

- 解决键盘弹起后消息列表被遮挡问题。

2019-03-04 &nbsp;&nbsp;&nbsp;&nbsp; v1.0.0

- 测试版。

## 已知问题

- ~~当消息为`?`、 `;`等符号时不会自动换行。（无解？）~~

- ~~用户开启匿名选项时进入退出聊天室时仍会发送系统消息。~~

## 未来计划

- ~~匿名昵称、头像。~~

- ~~输入框渲染优化。~~

- ~~交互动画。~~

- 更多的颜色主题。（添加主题真是一个又费时间有没有成就感的事）

- 自己写的后端程序。

- 用`Typescript`重构逻辑层
