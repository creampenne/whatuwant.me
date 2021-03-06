---
title: "[GitHub.io + Hugo] 블로그 개발기"
date: 2021-03-29
tags: ["github", "hugo", "html", "css", "scss", "js"]
draft: false 
---

### Static Site?  
웹사이트는 크게 **Dynamic site**와 **Static site**가 있어여  
**Dynamic site**는 동적 사이트로 그때그때 동적으로 html을 생성해서 보여줘  
즉, Dynamic site의 주소는 같지만 화면은 지속적으로 변할 수 있다~  
그에 반해 **Static site**는 고정된 html 그냥 뿌려주는 사이트!

많이 사용하는 YouTube, Instagram 등의 대부분 사이트들은 **Dynamic site**  
그러면 많은 사이트들이 Dynamic site를 사용함에도 불구하고 **Static site**를 개발했는지 장점들을 나열해 봅니당.

* #### Better Performance
    ##### 서버에 미리 저장된 파일만 클라이언트에게 전송하면 되기 때문에 속도가 빠르당

* #### Flexibility  
    ##### 코드를 모듈화하여 원하는 기능(ex.Pagination)을 간단하게 사이트에 올릴 수 있담

* #### Superior Security  
    ##### 서버 측 기능이 거의 없기 때문에 Scripting이나 DB 취약점을 통해 엑세스 할 수 없다!

이 외에도 많은 장점들이 있지만 사실상 이 세가지만으로도 내가 블로그를 개발하는 이유로 충분!

### Why Hugo?  
Hugo는 Jekyll, Hexo 등과 같은 static site generator 중 하나  
사실 Jekyll과 Hugo 중 어떤 걸 사용할지 고민을 오래 했던 것 같은데
Jekyll이 GitHub에서 공식적으로 후원도 하고 가장 많은 사람들이 사용하고 있고, 테마도 정말 많아서 좋아보임  
그런데 난 왜 Hugo를 골랐을까..?(조금 후회하고 있지만 만족,,)
Hugo의 장점들만 살펴보면 #빠르고 #Go언어를사용하고 #성장하는추세이고 #한글화된문서가적음  
> ###### 해외포럼이용빈도수높이기=~~삽질은 사랑입니다~~  

## Hugo Blog Installation

##### Download Choco
##### 사지방 컴퓨터가 윈도우라 choco 패키지 관리자를 사용하여 hugo 설치
~~~
$ Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
~~~
##### Download Hugo:
~~~
$ choco install hugo-extended -confirm
~~~
##### Set up the Site:
~~~
$ hugo new site Portfolio-Blog
~~~
##### Download Theme
**[Hugo-Theme-Codex](https://github.com/jakewies/hugo-theme-codex/) README.md 파일 참조**
##### Create Post
~~~
$ hugo new blog/:blog-post.md
~~~
##### Test the site locally
~~~
$ hugo server -D
~~~
여기까지가 Local에서 Hugo 블로그 셋업 과정!!!🐰


## Deploy to Git Pages

##### Remote / Submodule Settings
root 폴더로 이동:
~~~
$ git init
$ git remote add origin https://github.com/1-whateveruwant/Portfolio-Blog.git
$ git submodule add -b master https://github.com/1-whateveruwant/1-whateveruwant.github.io.git public
~~~

##### Build / Git push
~~~
$ hugo -t hugo-theme-codex
$ cd public
$ git add .
$ git commit -m "<커밋 메세지>"
$ git push origin master
$ cd ..
$ git add .
$ git commit -m "<커밋 메세지>"
$ git push origin master
~~~

**[whatuwant Blog](https://whatuwant.me) Build Check😎**

여기까지가 [GitHub Pages + Hugo] 블로그 개발 과정이고  
포스팅 내용만 보면 굉장히 간단한데 사실 디버깅을 정말 많이,,,  
~~자잘한 오류들로 주말 동안 또 삽질했네;~~  

그나저나 마크다운 문법 너무 쉬운데 기능이 적어서 아쉽다.  
뭔가 공식적인 문서에 쓰기 좋아서 일상글 쓰기 힘들듯,,  
개발하면서 생겼던 오류들은 다음 글에서 더 자세히 다루고 그다음 글에서는 블로그에 추가할 기능들에 대해 적어볼 예정!!  

그럼 ㅂㅏㅇl -! 빈센조 보러갈게여 -!
