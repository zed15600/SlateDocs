---
title: OwnLocal API Docs

language_tabs: # must be one of https://git.io/vQNgJ
  - shell

toc_footers:
  - <a href='https://github.com/slatedocs/slate'>Documentation Powered by Slate</a>

includes:
  - ads
  - errors

search: true

code_clipboard: true
---

# Introduction

Welcome to the OwnLocal API. You can use our API to access OwnLocal API endpoints.

You can view code examples in the dark area to the right.

# Authentication

> To authorize, use this code:

```shell
# With shell, you can just pass the correct header with each request
curl "api_endpoint_here" \
  -H "Authorization: <token>"
```

> Make sure to replace `<token>` with your API key.

OwnLocal uses API keys to allow access to the API. Contact our support team to get your API key.

OwnLocal expects for the API key to be included in all API requests to the server in a header that looks like the following:

`Authorization: <token>`

<aside class="notice">
You must replace <code><token></code> with your organization API key.
</aside>
