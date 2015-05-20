SLP-ChangeLog
=============

### 2015-05-20(v1.5.3)

#### New Features
* 异步导出数据量过大的记录

#### Resolved Issues
* 修复表单的模版消息推送 url 问题
* 修复全屏查看记录的样式问题
* 修复绑定限制

------

### 2015-05-08(v1.5.0)

#### New Features
* 新增模版消息
* 推送包
* 在信息流里同时展示消息和表单

#### Resolved Issues
* 暂无

------

### 2015-04-29(v1.4.9)

#### New Features
* 递增排序组织名字

#### Resolved Issues
* 修复关联组织和用户的缓存
* 修复当用户是消息的发布者当没向自己发送消息时的错误

------

### 2015-04-27(v1.4.8)

#### New Features
* 测试 JSON 缓存

#### Resolved Issues
* 暂无

------

### 2015-04-24(v1.4.7)

#### New Features
* 暂无

#### Resolved Issues
* 修复菜单
* 修复长组织名字的 bug

------

### 2015-04-23(v1.4.6)

#### New Features
* 取消绑定用户
* 异步导入记录

#### Resolved Issues
* 在生成环境下忽略 `exception_notification`

------

### 2015-04-22(v1.4.5)

#### New Features
* 显示空间绑定状态
* `web` 端使用和 `mobile` 相同的模版（文章）

#### Resolved Issues
* 修复当二维码不存在的时候的登陆问题

------

### 2015-04-20(v1.4.4)

#### New Features
* 组织以树状结构展示
* 导入名单过大时，异步处理

#### Resolved Issues
* 添加成员/协作者等组织名字过长的 bug
* 修改了部分样式
* 修复定向推送的面包屑

------

### 2015-04-15(v1.4.3)

#### New Features
* 添加了top_bar来显示page_title和菜单的toggler

#### Resolved Issues
* 修改了phone_require的渲染位置
* 修改了部分样式

------

### 2015-04-13(v1.4.1)

#### New Features
* 给 `web` 端的文章添加 `mobile` 端一样的样式

#### Resolved Issues
* 修复二维码登陆的 `js` 问题（未登陆时 `js` 都会报错)

------

### 2015-04-10(v1.4.0)

#### New Features
* 给表单添加抽屉功能`阅读统计`状态

#### Resolved Issues
* 暂无

------

### 2015-03-24(v1.3.7)

#### New Features
* 登陆的二维码将在 5 分钟后失效

#### Resolved Issues
* 暂无

------

### 2015-03-24(v1.3.6)

#### New Features
* 暂无

#### Resolved Issues
* 修复表单 `keyup` 事件（该问题可能会导致校验代码出问题）

------

### 2015-03-18(v1.3.3)

#### New Features
* 通讯录 1.0.0 版本（http://hereistheskylark.com/apps/contacts）

#### Resolved Issues
* 暂无

------

### 2015-03-17(v1.3.2)

#### New Features
* 为表格添加相应式
* 新的一年第一个版本

#### Resolved Issues
* 暂无

------

### 2015-02-14(v1.3.1)

#### New Features
* 将文章相关的页面的标题设置为空间名字

#### Resolved Issues
* 修复加载更多

------

### 2015-02-12(v1.3.0)

#### New Features
* 细分管理权限
* 其他（参见`commit`）

#### Resolved Issues
* 暂无

------

### 2015-02-01(v1.2.1)

#### New Features
* 升级 `nexmo-voice`

#### Resolved Issues
* 暂无

------

### 2015-01-28(v1.2.0)

#### New Features
* Landing page
* 新的微信推送模板
* 升级到 `Rails 4.2.0`
* 查看`已阅用户`

#### Resolved Issues
* 新的 `backbone modal`
* 表单填写相关 `bug`

------

### 2015-01-07(v1.1.4)

#### New Features
* 文章可以插入视频

#### Resolved Issues
* 暂无

------

### 2014-12-25(v1.1.2)

#### New Features
* 暂无

#### Resolved Issues
* 修复当子菜单为空时不能添加子菜单的 bug
* 修改更新组织成员的 api_url

------

### 2014-12-25(v1.1.2)

#### New Features
* 添加 `CLICL` 微信菜单
* 通过拖动来修改微信菜单的顺序
* 时间选择器起始时间改为`天`
* 加强的用户搜索（用`三`可以搜索到`张三`和`张三丰`）
* skip `v1.1.1`

#### Resolved Issues
* 修复数据迁移不能回滚
* 表单推送时显示无格式的描述文本
* 修复组织树形选择在 `fixfox` 下的兼容

------

### 2014-12-23(v1.1.0)

#### New Features
* 添加`名片`功能
* 很久没更新了

#### Resolved Issues
* 修复匿名填写成功时的页面错误

------

### 2014-12-01(v1.0.14)

#### New Features
* 提示用户填写电话号码

#### Resolved Issues
* 暂无

------

### 2014-11-26(v1.0.13)

#### New Features
* 使用树状结构展示组织选择器

#### Resolved Issues
* 修复`tagged_with`的计算错误
* 修复导出时身份证号码自动四舍五入的错误

------

### 2014-11-20(v1.0.12)

#### New Features
* 暂无

#### Resolved Issues
* 修复其他项的触发事件（导致“中文翻译为拼音”，其实是没有检测到`keyup`）
* 移除 mobile 端的`turbolinks`（导致 Android 图片预览等问题）

------

### 2014-11-17(v1.0.11)

#### New Features
* 文章分类排序功能

#### Resolved Issues
* 暂无

------

### 2014-11-10(v1.0.10)

#### New Features
* 暂无`（光棍节快乐）`

#### Resolved Issues
* 修复重复创建推送的问题
* 修复不能修改菜单的问题

------

### 2014-11-07(v1.0.9)

#### New Features
* 修改消息标签

#### Resolved Issues
* 修复`QR` size
* 修复微信菜单样式

------

### 2014-11-01(v1.0.8)

#### New Features
* 升级`sass`版本
* 添加`newrelic`

#### Resolved Issues
* 暂无

------

### 2014-10-31(v1.0.7)

#### New Features
* 新的flash alert（只调整了结构）

#### Resolved Issues
* 组织成员管理（members/edit）页面的`js`错误
* 微信消息，表单，文章等的图片预览的Bug

------

### 2014-10-27(v1.0.6)

#### New Features
* 添加客服功能支持

#### Resolved Issues
* 暂无

------

### 2014-10-26(v1.0.5)

#### New Features
* 添加错误提示当修改用户失败时

#### Resolved Issues
* 修复未读/未填分页
* 修复用户名片样式（及其他类似卡片）

------

### 2014-10-20(v1.0.4)

#### New Features
* 搜索不在任何组织的成员
* 导入时自动关联和更新已存在的用户

#### Resolved Issues
* 重新设计`user`的`model`（backbone）

------

### 2014-10-13(v1.0.3)

#### New Features
* 搜索组织成员分类

#### Resolved Issues
* 修复`fast-click`

------

### 2014-10-11(v1.0.2)

#### New Features
* 搜索组织成员

#### Resolved Issues
* 修复表单`其他选项`样式

------

### 2014-10-08(v1.0.1)

#### New Features
* 导出绑定情况

#### Resolved Issues
* 修复表单页面的样式问题

------

### 2014-09-30(v1.0.0)

#### New Features
* 允许注册

#### Resolved Issues
* 暂无

------

### 2014-09-29(v0.9.3)

#### New Features
* 为 category 添加 icon
* 签到验证可以为某个范围的 IP

#### Resolved Issues
* 修复绑定样式
* 修复菜单的一些 BUG

------


### 2014-09-24(v0.9.2)

#### New Features
* 同步菜单到微信服务器
* 为每个 namespace 增加 LOGO
* CMS 新的菜单样式

#### Resolved Issues
* 暂无

------


### 2014-09-24(v0.9.1)

#### New Features
* CMS 渲染添加附件

#### Resolved Issues
* 暂无

------


### 2014-09-23(v0.9.0)

#### New Features
* 新的 CMS

#### Resolved Issues
* 修复 CMS 相关的样式

------

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
