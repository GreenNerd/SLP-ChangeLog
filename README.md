SLP-ChangeLog
=============

### 2014-09-16(v0.8.7)

#### New Features
* 进入公众帐号立即提醒未处理的消息

#### Resolved Issues
* 修复表单导出在 Windows 下的样式

------


### 2014-09-10(v0.8.6)

#### New Features
* 新增标记字段
* 新的表单导出样式
* `wechat`端的单次提交限制

#### Resolved Issues
* 修复导入名单过多时的 JS 错误
* 修复分页 bug

------


### 2014-09-05(v0.8.5)

#### New Features
* 指定电话推送的号码

#### Resolved Issues
* 修复树状选择器的样式

------


### 2014-09-05(v0.8.4)

#### New Features
* 签到功能
* 树状选择器
* 组织权限继承

#### Resolved Issues
* 增强权限继承及限制修改

------

### 2014-09-01(v0.8.3)

#### New Features
* 新的分页器
* 添加不在任何组织的成员
* 组织权限继承

#### Resolved Issues
* 暂无

------


### 2014-08-28(v0.8.2)

#### New Features
* 暂无

#### Resolved Issues
* 解决新建用户报错信息问题

------

### 2014-08-28(v0.8.1)

#### New Features
* 新的提醒插件
* 表单记录导入时，改用组织和用户的名字
* 重写前端`backbone`分页

#### Resolved Issues
* 解决绑定用户时取不到资料的问题

------

### 2014-08-27(v0.8.0)

#### New Features
* 添加标签功能（可以给用户，消息，表单添加标签）
* 管理员可以修改用户资料
* 添加填写表单成功的提示

#### Resolved Issues
* 修复下载组织编号的问题
* 修复多图上传的问题

------


### 2014-08-21(v0.7.14)

#### New Features
* 重写了富文本的图片上传（允许一次传多张图片）
* 修改了附文本的部分样式
* 合并了最新版本的simditor
* 重写了uploader

#### Resolved Issues
* 隐藏删除按钮，当没有权限时

------


### 2014-08-13(v0.7.13)

#### New Features
* 增加对 IE 的支持

#### Resolved Issues
* 修复`wechat端`的`overflow`问题

------


### 2014-08-13(v0.7.12)

#### New Features
* 添加`再填一份`快捷入口
* 组织页面展示绑定人数

#### Resolved Issues
* 表单新建/修改页面不能删除表项

------


### 2014-08-08

#### New Features
* 组织删除功能
* 消息和表单删除功能
* 语音服务器改为`Nexmo`

#### Resolved Issues
* 文件上传字段删除附件的 BUG

------


### 2014-08-07

#### New Features
* 表单填写页面渲染附件

#### Resolved Issues
* 无

------


### 2014-08-05

#### New Features
* 表单可以添加附件
* 表单的描述可以为富文本

#### Resolved Issues
* 无

------


### 2014-08-04

#### New Features
* 添加**文件上传**字段

#### Resolved Issues
* 移除名字，识别码和手机号中多余的空格
* 导入时，字段错位

------


### 2014-08-01

#### New Features
* 字段添加管理员可填和可修改属性
* 可以用手机和识别码二选一绑定
* 权限限制时，添加自动登录

#### Resolved Issues
* 用户端的表格溢出问题

------


### 2014-07-31

#### New Features
* 消息可以添加附件
* 文章可以添加附件

#### Resolved Issues
* 新的编辑器的一些 BUG

------


### 2014-07-27

#### New Features
* 新的时间选择器（推送）

#### Resolved Issues
* 无

------


### 2014-07-25

#### New Features
* 新的编辑器
* 下载组织编号（导入记录相关）

#### Resolved Issues
* 微信推送时链接`pushable.id`问题

------


### 2014-07-24

#### New Features
* 相关记录推送

#### Resolved Issues
* 电话推送 SSL 问题
* 删除失败的推送

------


### 2014-07-20

#### New Features
* 导入表单
* 表单记录可以指定用户或个人
* 新的添加一条记录功能
* 新的表单修改和查看
* 用户可以管理自己的填写记录（表单），添加，删除，修改

#### Resolved Issues
* 表单修改时自动选择所有文字只在第一次点击时生效
* 解决已绑定用户被剔除的问题
* 解决 Windows Phone 不发送 `POST` 请求（登陆时）
