SLP-ChangeLog
=============

### 2015-11-18(v1.8.3)

#### New Features
* 暂无

#### Resolved Issues
* Fix removing association when organizations are destroyed
* Fix vars overflow of the template_post
* Fix cascaded_select endpoint for the normal user

------

### 2015-11-11(v1.8.3.alpha)

#### New Features
* 增加提交表单后`展示统计结果`
* 初始化 Namespace 时同步已有微信的菜单，而不是直接覆盖
* 新增`以组织名义发送`
* 新增`组织名片`

#### Resolved Issues
* 修复只有文章权限的管理员不能进入后台的 bug
* 修复`选择焦点乱跳`问题

------

### 2015-11-05(v1.8.2)

#### New Features
* 复制`模板通知`
* 分离`手动`和`自动`追加消息的逻辑
* 重写申请加入组织的申请页面
* 添加`组织字段`
* 优化导出级联选择


#### Resolved Issues
* 修复转移用户时不转移`模板通知`
* 修复编辑用户不能修改标签的 bug
* 尝试修复`选择焦点乱跳`问题

------

### 2015-10-25(v1.8.1)

#### New Features
* 给文章添加排序：`手动排序`、`创建时间降序`、`创建时间升序`
* 给下来选项添加一个空值，`请选择`引导用户选择

#### Resolved Issues
* 限定绑定用户对于`开启只能填写一次开关的表单`只能填写一次
* 修复编辑器添加链接时，不能修改链接的问题
* 修复表单不能复制的问题

------

### 2015-10-24(v1.8.0)

#### New Features
* 级联选择
* 向新成员追加消息
* 优化消息的预览
* 导出消息阅读/填写状态

#### Resolved Issues
* 修改单选和多选导入的分隔符为`分号`
* 修复当用户不在任何组织时导出表单的排版异常

------

### 2015-10-19(v1.7.12)

#### New Features
* 暂无

#### Resolved Issues
* 修复模板消息中记录的渲染顺序（*上传顺序*）
*  修复了标签页面的模板通知的路由问题

------

### 2015-10-08(v1.7.10)

#### New Features
* 给模板消息（*草稿箱*）的记录添加分页

#### Resolved Issues
* 导入记录时，只给`已发布的表单或模板通知`的`关联用户`发送通知

------

### 2015-09-30(v1.7.8)

#### New Features
* 给`模板通知`添加标签

#### Resolved Issues
* 修复导入别名为纯数字的导入
* 优化发送`模板通知`

------

### 2015-09-28(v1.7.7)

#### New Features
* 消息抄送给作者和写作者

#### Resolved Issues
* 修复消息中表单不能更改宽度的 bug
* 修复表单重复提交的问题
* 修复`导入表单模板.xls`的下载
* 修复多选和单选复制时选项复制失败的问题
* 修复表单接收者人数计算问题

------

### 2015-09-27(v1.7.6)

#### New Features
* 模板消息新增`循环表单`

#### Resolved Issues
* 暂无

------

### 2015-09-25(v1.7.5)

#### New Features
* 暂无

#### Resolved Issues
* 修复表单定向推送名单（`此功能在未来会移除，请使用模板消息`）

------

### 2015-09-25(v1.7.4)

#### New Features
* 模板通知
* 导出组织成员
* 为用户添加`导入别名`，管理员可修改，解决用户重名问题

#### Resolved Issues
* 修复 bugs
* 用户在 10 分钟内只会收到一次未读提醒（开启微信定位上报时）

------

### 2015-09-14(v1.7.3)

#### New Features
* 添加`转发微信请求地址`

#### Resolved Issues
* 暂无

------

### 2015-09-06(v1.7.2)

#### New Features
* 重构组织权限，权限自动向下覆盖，且上级创建者对下级所有组织有所有权限，空间管理员可以操作所有组织
* 可以设定用户申请加入组织后的行为（*审核后加入*、*自动加入*、*禁止申请*）

#### Resolved Issues
* 修复标签消息页面的缓存

------

### 2015-08-24(v1.7.1)

#### New Features
* 申请加入组织

#### Resolved Issues
* [hot] 空间管理员对组织有所有的权限

------

### 2015-08-11(v1.7.0)

#### New Features
* 添加 otth2 认证（授权给第三方应用）

#### Resolved Issues
* 修复`有权限访问的文章和分类`不能返回正确内容的问题

------

### 2015-08-10(v1.6.17)

#### New Features
* 为文章添加分页（变量参考 [分页](https://github.com/GreenNerd/SLP-ChangeLog/blob/master/CMS%20liquid.md#paginator "分页")）
* 添加`用户只能看见自己有权限查看的分类和文章`的功能（此功能没有考虑不在当前空间的用户）

#### Resolved Issues
* 修复异步发送回执时，推送包过早创建并执行的 bug

------

### 2015-08-06(v1.6.16)

#### New Features
* 添加 `已关闭的消息/表单` 的页面

#### Resolved Issues
* 修复向大量组织发送表单和消息出现 `超时` 的 bug

------

### 2015-08-05(v1.6.15)

#### New Features
* 暂无

#### Resolved Issues
* 修复关闭 `form` 的 bug

------

### 2015-07-30(v1.6.14)

#### New Features
* 缓存了 `form` 和 `post`
* 添加了 `章节` 字段
* 添加了 `整数` 字段

#### Resolved Issues
* 修复报表页面的 NaN 错误

------

### 2015-07-23(v1.6.11)

#### New Features
* 文章和分类可以自定义模板
* 新增 `403`（没有权限页面模板） 和 `404`（没有找到页面模板） 页面，如果留空则用系统自带的，变量参见 [变量](https://github.com/GreenNerd/SLP-ChangeLog/blob/master/CMS%20liquid.md#currentuser)
* 为文章添加权限

#### Resolved Issues
* 修复标签消息/表单页面的样式
* 修复添加下级组织的样式

------

### 2015-07-20(v1.6.10)

#### New Features
* 给表单字段添加样式
* 移除滑动呼出菜单的方式
* 自动移除模板消息 ID 前后的空白字符（空格）

#### Resolved Issues
* 修复输入框聚焦时被键盘遮挡的bug

------

### 2015-07-17(v1.6.9)

#### New Features
* 空间管理员可以删除`不在任何组织的成员`

#### Resolved Issues
* 修复不能修改表单标签的 bug

------

### 2015-07-14(v1.6.8)

#### New Features
* 关闭表单
* 添加`填写后`功能（默认，文案，跳转地址）

#### Resolved Issues
* 修复文章内嵌表单 option 样式
* 修复微信推送失败无限重试的问题
* 允许未登录用户在微信里面下载附件
* 修复多次提交问题

------

### 2015-07-05(v1.6.7)

#### New Features
* 给报表添加缓存

#### Resolved Issues
* 修复欢迎消息图片的比例
* 修复了些报表的缓存问题

------

### 2015-07-01(v1.6.6)

#### New Features
* 表单添加报表功能（限单选和多选）

#### Resolved Issues
* 修复 layout 缺失时不能渲染的问题

------

### 2015-06-30(v1.6.5)

#### New Features
* 可以复制表单
* 添加备案信息
* 导出记录时，为附件字段添加链接
* 单选/多选选项可以选择样式

#### Resolved Issues
* 修复当表项过多时导出记录超时
* 修复匿名下载附件不成功的 bug

------

### 2015-06-24(v1.6.4)

#### New Features
* 不限制标记字段，如果手动设置
* 用户可以转移组织给另一个人
* 空间管理员可以转移一个人的所有相关的资源给另一个人

#### Resolved Issues
* 修复不能取消用户的所有标签
* 修复未读人数
* 修复分步填写的 bug

------

### 2015-06-15(v1.6.3)

#### New Features
* 添加了些缓存加速表单和消息的首页
* 首页添加跳转下一屏的箭头

#### Resolved Issues
* 允许普通用户填写表单时上传附件

------

### 2015-06-06(v1.6.2)

#### New Features
* 新的下载方式，可以跳转到浏览器打开
* 为文章加入权限
* 通过文件导入表项

#### Resolved Issues
* 修复电话号码为空时可以被任意用户登录的问题
* 修复草稿的组织初始化问题
* 取消分类名字唯一性校验

------

### 2015-06-02(v1.6.0)

#### New Features
* 添加草稿箱
* 表单得分步填写
* 富文本编辑器添加锚点和 tab
* 指定用户标签和组织成员才看文章分类

#### Resolved Issues
* 修复模版消息

------

### 2015-05-26(v1.5.4)

#### New Features
* 优化滑动菜单

#### Resolved Issues
* 修复一些样式
* 修复 wx jssdk 问题

------

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
