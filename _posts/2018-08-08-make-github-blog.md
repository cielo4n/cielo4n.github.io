---
title: GitHub Blog
date: 2018-08-08
description: 깃허브 블로그 / 지킬테마 / 로컬 서버에서 확인
categories:
 - git
tags:
 - github
 - gitblog
 - jekyll
 - ruby
 - gem
---


# 깃허브 블로그 만들기

깃허브 블로그에 지킬 테마를 적용한 후
로컬에서 확인하며 사용하려고 한다.

---

## 1. 깃허브에서 repository 생성
<https://github.com/>
repository 계정이름을 `{아이디}.github.io` 로 생성한다

## 2. 지킬 테마 찾기
<http://jekyllthemes.org/>
사용할 테마를 복제해오거나 다운로드 받아 폴더에 넣는다.
```sh
git clone https://github.com/Simpleyyt/jekyll-theme-next.git
```

## 3. 저장소에 올려 지킬테마 확인

폴더를 git으로 버전관리하고 나의 repository와 연결한다.
```sh
git init
git remote add origin https://github.com/cielo4n/cielo4n.github.io.git 
```
변경된 내용을 원격저장소에 올린다.
```sh
git add .
git commit -m '커밋 메세지'
git push origin master
```
자신의 깃페이지 `https://{아이디}.github.io/`에서 올라간 지킬테마를 확인해 볼 수 있다


## 4. 로컬서버에서 실행해보기
* 루비 설치 (<http://rubyinstaller.org/downloads/>)

환경변수가 설정되어 있지 않을 경우 설정해준다. 
(내가 다운로드 받은 버전은 [Ruby+Devkit 2.4.4-2 (x64)]이다.)
```sh
ruby --version
gem install bundler
bundle install
bundle exec jekyll serve
```
아마 위 순서대로 설치하고 `http://127.0.0.1:4000` 로 접속하면 로컬에서의 페이지가 실행될 것이다.

혹시 실행되지 않을 경우 내가 이전에 설치했던 것을 적어놓는다.
```sh
gem install jekyll
gem install rouge
```
---
>## 참고 사이트
>
>[깃허브 페이지로 블로그 만들기](https://github.com/gjchoi/gjchoi.github.io/blob/master/_posts/2016-02-18-Github-page%EB%A1%9C-%EB%B8%94%EB%A1%9C%EA%B7%B8-%EB%A7%8C%EB%93%A4%EA%B8%B0.md)  
>[지킬 공식 사이트](http://jekyllrb.com/)  
>[https://github.com/Simpleyyt/jekyll-theme-next](https://github.com/Simpleyyt/jekyll-theme-next/blob/master/README.en.md)