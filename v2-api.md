## 认证
2种方式：
- 传private_token参数
- 传PRIVATE-TOKEN http 头

## 分页
所有返回集合的都有分页
参数：
- page 页数
- per_page 每页个数，默认25

## API
## 用户
| 字段      |    类型 | 解释  |
| :-------- | :--------| :--: |
| name  | string |  名字   |
| nickname  | string |  昵称   |
| sex  | integer |  性别：1-男，2-女，0-未知   |
| phone  | string |  电话号码   |
| identifier  | string |  识别码   |
| headimgurl  | string |  头像url   |

### 获取用户集合
> GET /users

### 获取单个用户
> GET /users/:id

## 组织
| 字段      |    类型 | 解释  |
| :-------- | :--------| :--: |
| name  | string |  名称   |
| description  | string |  描述   |
| created_at  | string |  创建时间   |
| children_count  | integer |  下级组织数   |
| parent_id  | integer |  上级组织id   |

### 获取组织集合
> GET /organizations

### 获取单个组织
> GET /organizations/:id

### 获取某个组织成员集合
> GET /organizations/:id/members

### 获取某个组织的下属组织集合
> GET /organizations/:id/children

### 获取根组织集合
> GET /organizations/root

## 普通通知
| 字段      |    类型 | 解释  |
| :-------- | :--------| :--: |
| title  | string |  标题   |
| html_body  | string |  内容   |
| created_at  | string |  创建时间   |


### 获取普通通知集合
> GET /posts

参数：
- status，可选值（drafted, published, closed）分别表示：草稿，发布，关闭。不传表示全部


### 获取单个普通通知
> GET /posts/:id

### 获取某个普通通知的评论集合
**评论**
| 字段      |    类型 | 解释  |
| :-------- | :--------| :--: |
| body  | string |  内容   |
| created_at  | string |  创建时间   |
| user  | hash |  评论者   |
| reply  | hash |  回复   |


> GET /posts/:id/comments

### 获取某个普通通知的接受者集合
> GET /posts/:id/receipts

## 表单
| 字段      |    类型 | 解释  |
| :-------- | :--------| :--: |
| title  | string |  标题   |
| description  | string |  描述   |
| created_at  | string |  创建时间   |
| fields  | array |  表单所有字段，字段详细信息见下面   |
| author  | hash |  创建者，信息跟users相同   |
| attachments  | array |  附件，信息见下面   |
| tags  | array |  标签，信息见下面   |

**fields 信息**

| 字段      |    类型 | 解释  |
| :-------- | :--------| :--: |
| title  | string |  标题   |
| description  | string |  描述   |
| type  | string |  字段类型，详细信息见下面   |
| validations  | array |  验证，有`presence`表示必填   |
| other_option  | boolean |  用于单多选，true: 有其他选项，false: 没有其他选项   |
| maximum  | integer |  用于评分字段，表示最大评分   |
| longitude  | float |  用于定位字段，表示目标位置的经度   |
| latitude  | float |  用于定位字段，表示目标位置的纬度   |
| max_distance  | integer |  用于定位字段，表示于目标位置的最大距离，单位m   |
| remark  | string |  用于定位字段，表示于目标位置的名称   |
| detail_id  | integer |  用于明细字段，如果存在表示，是明细字段里面的一个字段   |
| children  | array |  用于明细字段，表示明细字段里面所有的字段   |
| options  | array |  用于单多选，表示选项信息   |

**field type**

|    type 类型 | 解释  |
| :--------| :--: |
| Field::Rating | 评分 |
| Field::Location | 定位  |
| Field::CascadedSelect | 级联选择 |
| Field::TextField | 文本 |
| Field::RadioButton | 单选 |
| Field::SectionBreak | 分割线 |
| Field::CheckBox | 多选 |
| Field::TextArea | 段落 |
| Field::Detail | 明细 |
| Field::Integer | 整数 |
| Field::File | 文件上传 |

**options 信息**

| 字段      |    类型 | 解释  |
| :-------- | :--------| :--: |
| value  | string |  选项值   |

**attachments 信息**

| 字段      |    类型 | 解释  |
| :-------- | :--------| :--: |
| name  | string |  附件名称   |
| size  | string |  大小   |
| mime_type  | string |  类型   |

**tags 信息**

| 字段      |    类型 | 解释  |
| :-------- | :--------| :--: |
| name  | string |  名称   |


### 获取表单集合
> GET /forms

参数：
- status，可选值（drafted, published）分别表示：草稿，发布。不传表示全部

### 获取单个表单
> GET /forms/:id

### 获取某个表单的评论集合
> GET /forms/:id/comments

### 获取某个表单的接受者集合
> GET /forms/:id/receipts

### 获取某个表单的填写记录集合
**填写记录**
| 字段      |    类型 | 解释  |
| :-------- | :--------| :--: |
| created_at  | string |  创建时间   |
| entries  | array |  每个字段对应的填写值   |
| user  | hash |  填写者，没有则是匿名填写   |
| involved_users  | array |  用于模板消息，由管理员填写   |
| involved_organizations  | array |  用于模板消息，由管理员填写   |

**entries 信息**
| 字段      |    类型 | 解释  |
| :-------- | :--------| :--: |
| created_at  | string |  创建时间   |
| value  | string |  填写的对应字段的值   |
| field_id  | integer |  对应字段id   |
| option_id  | integer |  用于单多选，对应选项id   |
| choice_id  | integer |  用于级联选择   |
| latitude  | float |  用于定位字段，定位到的经度   |
| longtitude  | float |  用于定位字段，定位到的纬度   |
| group_id  | integer |  用于明细字段，分组   |
| attachment  | hash |  用于文件上传字段，上传文件的相关信息   |


> GET /forms/:id/responses

## 模板通知
| 字段      |    类型 | 解释  |
| :-------- | :--------| :--: |
| title  | string |  标题   |
| html_body  | string |  内容   |
| fields  | array |  表单所有字段   |
| author  | hash |  创建者，信息跟users相同   |
| attachments  | array |  附件   |
| tags  | array |  标签   |



### 获取模板通知集合
> GET /template_posts

参数：
- status，可选值（drafted, published）分别表示：草稿，发布。不传表示全部

### 获取单个模板通知
> GET /template_posts/:id

### 获取某个模板通知的评论集合
> GET /template_posts/:id/comments

### 获取某个模板通知的接受者集合
> GET /template_posts/:id/receipts

### 获取某个模板通知的填写记录集合
> GET /template_posts/:id/responses
