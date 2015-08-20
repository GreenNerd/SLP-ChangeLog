## Attributes
### Base
- id (`integer`)

### Home
- name (`string`)
- categories (`associations`)
- root_categories (`associations`)

### Category
- name (`string`)
- icon (`string`)
- description (`string`)
- created_at (`datetime`)
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

### Page
- title (`string`)
- description (`string`)
- html_body (`text`)
- hidden(`boolean`)
- external_link (`string`)
- external_link? (`boolean`)
- created_at (`datetime`)
- hidden(`boolean`)
- category (`association`)
- url (`string`)
- cover (`string`)
- cover? (`boolean`)
- attachments (`associations`)

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

### Paginator
- per_page(`integer`)*每页的数量*
- current_page(`integer`)*当前的页码数*
- total_pages(`integer`)*总共的页码数*
- previous_page_link(`string`)*上一页的地址*
- current_page_link(`string`)*当前页的地址*
- next_page_link(`string`)*下一页的地址*

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
