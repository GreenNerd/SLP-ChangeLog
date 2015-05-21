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

### Page
- title (`string`)
- description (`string`)
- html_body (`text`)
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

## Request

1. `GET /categories`
    > `skylark_cms.home`
1. `/categories/:category_id`
    > `skylark_cms.category`

1. `GET /categories/:category_id/pages/:page_id`
    > `skylark_cms.page`
