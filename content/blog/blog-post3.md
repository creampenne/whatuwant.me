---
title: "[GitHub.io + Hugo] 디버깅 정리"
date: 2021-04-12
tags: ["github", "hugo", "html", "css", "scss", "js"]
draft: true
---

MediaType.Suffix 오류 수정  

After Format
======================================================================
git clone https://github.com/1-whateveruwant/Portfolio-Blog.git

git rm --cached public

git submodule add https://github.com/1-whateveruwant/1-whateveruwant.github.io.git public

git rm --cached themes/hugo-theme-codex

git submodule add https://github.com/jakewies/hugo-theme-codex.git themes/hugo-theme-codex
