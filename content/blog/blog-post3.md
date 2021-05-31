---
title: "[GitHub.io + Hugo] 디버깅 정리"
date: 2021-04-20
tags: ["github", "hugo", "html", "css", "scss", "js"]
draft: false
---

MediaType.Suffix 오류 수정  
======================================================================
hugo-theme-codex/layouts/_default/baseof.html
~~~
{{ range .AlternativeOutputFormats }} 
  {{ printf `<link rel="%s" type="%s+%s" href="%s" title="%s" />` .Rel .MediaType.Type .MediaType.FirstSuffix.Suffix .Permalink $.Site.Title | safeHTML }} 
  {{ end }}
~~~
MediaType.Suffix to MediaType.FirstSuffix.Suffix


After Format
======================================================================
git clone https://github.com/1-whateveruwant/Portfolio-Blog.git

git rm --cached public

git submodule add https://github.com/1-whateveruwant/1-whateveruwant.github.io.git public

git rm --cached themes/hugo-theme-codex

git submodule add https://github.com/jakewies/hugo-theme-codex.git themes/hugo-theme-codex
