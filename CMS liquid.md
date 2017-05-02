## Attributes
### Base
- id (`integer`)

### Home
- name (`string`)
- ~~categories (`associations`)~~
- root_categories (`associations`)

### Category
- name (`string`)
- icon (`string`)
- description (`string`)
- created_at (`datetime`)
- updated_at (`datetime`)
- hidden(`boolean`)
- url (`string`)
- parent (`association`)
- root (`association`)
- ancestors (`associations`)
- children (`associations`)
- pages (`associations`)
- hidden(`boolean`)
- external_link(`string`)
- external_link?(`boolean`)
- cms_variables (`object`)

### Page
- title (`string`)
- description (`string`)
- html_body (`text`)
- hidden(`boolean`)
- external_link (`string`)
- external_link? (`boolean`)
- created_at (`datetime`)
- updated_at (`datetime`)
- hidden(`boolean`)
- category (`association`)
- url (`string`)
- cover (`string`)
- cover? (`boolean`)
- attachments (`associations`)
- read_count (`integer`)
- cms_variables (`object`)

### Attachment
- name (`string`)
- size (`string`)
- mime_type (`string`)
- url (`string`)

### CurrentUser
- name (`string`)
- nickname (`string`)
- phone (`string`)
- identifier (`string`)
- headmigurl (`string`)
- openid (`string`)
- from_wechat(`boolean`)

### Paginator
- per_page(`integer`)*每页的数量*
- current_page(`integer`)*当前的页码数*
- total_pages(`integer`)*总共的页码数*
- previous_page_link(`string`)*上一页的地址*
- current_page_link(`string`)*当前页的地址*
- next_page_link(`string`)*下一页的地址*

### Search
- categories(`category`)
- pages(`page`)
- query

## Request

1. 首页 `GET /categories`
    - `skylark_cms.home`
    - `skylark_cms.current_user`

1. 分类页面 `/categories/:category_id`
    - `skylark_cms.category`
    - `skylark_cms.current_user`
    - `skylark_cms.paginator`

1. 文章页面 `GET /categories/:category_id/pages/:page_id`
    - `skylark_cms.page`
    - `skylark_cms.current_user`
    - `skylark_cms.page.cms_variables.foo` （`"bar"`，cms_variables 设置： `{ "foo": "bar" }`）

1. 搜索 `GET /categories/:category_id/search`
    - params:
        - query
    - return
        - `skylark_cms.categories`
        - `skylark_cms.pages`
        - `skylark_cms.query`

# 消息的异常

## 404/403
- current_user

## 变量的空间
- skylark_message_exception

### 例子：
- `skylark_message_exception.current_user.name`


# 自定义 filters

### images

#### crop images

**用法：**
- `{{ 'a.png' | crop_image: 'main' }}` #=> `a.png?imageView/2/w/360/q/85`
- 自定义尺寸 `{{ 'a.png' | crop_image: 'imageView/2/w/360' }}` #=> `a.png?imageView/2/w/360`

**可选尺寸：**
- main: `imageView/2/w/360/q/85`
- cover: `imageMogr2/thumbnail/!640x320r/gravity/Center/crop/640x320`
- logo: `imageView2/1/w/132/h/132/q/85`
- welcome: `imageMogr2/thumbnail/!360x200r/gravity/Center/crop/360x200`
- small_welcome: `imageMogr2/thumbnail/!50x50r/gravity/Center/crop/50x50`

### HumanSize
**用法：** `{{ 1222222222 | human_size }}` #=> `1.1 GB`
