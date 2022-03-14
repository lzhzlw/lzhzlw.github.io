# Xiaoyang Li - AcadHomepage

forked from [RayeRen/acad-homepage.github.io](https://github.com/RayeRen/acad-homepage.github.io)

## 使用方法
### 修改个人信息

修改`_config.yml`里`site`和`author`相关的条目信息，不赋值的条目则不显示


### 修改现有页面

按照[markdown](https://markdown.com.cn/basic-syntax/)格式修改`_pages/`目录里的各个`.md`文件内容

当前`_pages/`目录包括：
- `about.md` 主页内容
- `publications.md` publications页面内容
- `reviewer_activities.md` reviewer activities页面内容
- `tpc_membership.md` TPC membership页面内容


### 新增页面

#### 1. 修改导航菜单
修改`_data\navigation.yml`，严格控制缩进，**新增**菜单的条目。新增的话参考下方`A NEW ITEM`的格式

```yml
# main links links
main:
  - title: "Publications"
    url: "/publications/"

  - title: "Reviewer Activities"
    url: "/reviewer_activities/"

  - title: "TPC Membership"
    url: "/tpc_membership/"
    
    # 增加一个菜单
    # Title为显示的菜单标题
    # url为子页面的链接后缀，需要和后面的步骤一致
  - title: "A NEW ITEM"
    url: "/a_new_item/"
```

#### 2. 新增子页面
在`_pages/`目录下新建一个`.md`文件，例如`a_new_item.md`，具体格式如下。
  - 主要分为最上方的参数段和下方的内容段。
  - 参数段其中`permalink`字段要与`_data\navigation.yml`中新建的`url`一致，`title`为子页面的标题，剩下两个默认即可。
  - 内容段用markdown格式写即可。

```
---
permalink: /a_new_item/
title: "A NEW ITEM"
excerpt: ""
author_profile: true
---

# First title

this is a new line

this is another new line

## second title

new line

### third title

new line

```


### 删除页面

#### 1. 删除导航菜单

修改`_data\navigation.yml`，删除某个条目(`title`和`url`)。


#### 2. 删除子页面

在`_pages/`目录下删除对应的`.md`文件。