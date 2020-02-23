---
title: Artifact
date: 2020-02-10 16:18:05
tags: ["npm", "package"]
category: ["front-end"]
---

# 簡介

Azure DevOps 中提供 Packages 存取及管理的服務。

# 緣由

因前端開發需求(vue plugin 共享)，需要一個提供**npm**存取及管理的服務並需要**private**的權限管制，進一步研究後發現公司現行的 **Azure DevOps** 就有此類的服務，故就不用 npm 官方需要付費的組織方案了。

# Organization Scoped Feed

因為一直嘗試想要建立一個組織層級的 feed 提供大家存取 NPM，但始終找不到使用者介面，終於在爬了許久的文中，找到了目前的解法(API request)。

在經歷千辛萬苦之後，發現需要忽略 project 的 path uri，僅需要提供組織名稱去做 post，並且要記得授權，最終我嘗試的結果是使用 PAT(persional access token)置換到 postman 的 b]Basic Athentification 的 user 及 password 中。

[azure devOps artifact feed doc](https://docs.microsoft.com/en-us/rest/api/azure/devops/artifacts/feed%20%20management/create%20feed?view=azure-devops-rest-5.1)
