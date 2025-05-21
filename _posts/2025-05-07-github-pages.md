---
title: GitHub Pages 개설하기
description: chripy 테마로 GitHub Pages 개설하기
author: nji
date: 2025-05-07 11:45:00 +0900
categories: [Blogging, Tutorial]
tags: [writing]     # TAG names should always be lowercase
toc: true
---

> 언젠간 해야지 해야지 하던 숙제를 드디어 하는 기분입니다
>
> velog, tistory, 네이버 블로그, GitHub Pages 등 여러 플랫폼을 고민하다가 내 친구 chatGPT의 추천으로 GitHub Pages로 선택하게 되었습니다.

# Jekyll 과 GitHub Pages

우선 블로그를 만들때 제가 사용할 도구는 `Jekyll`입니다. 

>`Jekyll`은 루비 기반 정적 사이트 생성기입니다.

제가 개설하면서 참고한 여러 블로그에서는 일단 `루비`와 `Jekyll`을 다운받고 시작했는데, 저는 그럴 필요가 없다고 생각해서 순서를 좀 바꿔보겠습니다.

## Jekyll 테마 선택

제일 먼저 해야할건 `Jekyll` 테마를 선택하는 겁니다.

다양한 사이트에서 테마를 선택할 수 있는데, 여러 사이트를 비교해 본 결과 굳이 그럴 필요가 없다고 생각합니다.

그냥 제일 보기 편한 사이트에서 테마를 고르면 될거 같습니다.

[테마 사이트](http://jekyllthemes.org/)

![theme](/assets/img/github_pages/theme.png)

<del>귀찮아서 링크 하나만 추가한거 맞아요. Jekyll theme 검색하면 많이 뜹니다</del>

> Demo를 누르면 미리보기가 가능하니 테마 고를때 참고하세요

![not_pure_poole](/assets/img/github_pages/notpurepoole.png)

제가 처음에 고른 테마는 `Not Pure Poole` 테마입니다. 전체적으로 심플하면서 적당한 커스터마이징도 가능한 부분이 마음에 들었습니다.

<del>홍대병이 있어서 사람들이 많이 사용하지 않는 테마라는 점도 마음에 들었습니다.</del>

![first_blog](/assets/img/github_pages/first_blog.png)

그리고 실제로 어느정도 꾸며서 블로그 포스팅 준비를 다 마친 상황이었습니다.

하지만... 게시글 목록을 볼때 아래 페이지 번호를 표기해주는 것이 아닌 Older, Newer만 표기되는 점이 너무 마음에 안들었고, 제 실력으로는 수정이 불가능했습니다

그래서 `Chripy` 테마로 다시 선택하게 되었습니다.

<del>유명한 테마는 역시 이유가 있는거 같습니다. 홍대병보단 커스터마이징이 우선인지라..</del>

![chripy](/assets/img/github_pages/chripy.png)

## Repository 생성, 빌드

테마를 다 골랐으면 고른 테마의 **Homepage**를 누르면 됩니다.

![homepage](/assets/img/github_pages/homepage.png)

이제 GitHub Repository가 뜨면 그 Repository를 복사해서 제 GitHub Repository를 만들어주면 됩니다.

> `chripy`테마는 해당 github의 `chripy-starter` repository를 가져오는걸 추천합니다

![starter](/assets/img/github_pages/starter.png)

여기서 **fork**해서 repository를 가져오는 방법이 있고, **ZIP 파일**로 다운을 받아서 Repository에 넣어주는 방법이 있습니다.

처음 개설할때는 fork하는 방법을 사용했는데, GitHub 잔디가 안심겼습니다. 그 문제를 해결하는 과정도 귀찮았고, 어떤 블로그를 보면서 따라한거라 방법도 잘 기억이 안나기 때문에 ZIP 파일을 다운받도록 하겠습니다.

![zip](/assets/img/github_pages/zip.png)

다운을 받았으면 Repository를 생성하고 이름을 `GitHub username.github.io`로 설정해주시면 됩니다.

그 후 다운받은 파일의 압축을 풀고 **모두 복사**해서 생성한 Repository에 넣어주면 됩니다.

---

저는 착하니까 fork하는 방법도 포스팅하겠습니다.

![fork](/assets/img/github_pages/fork.png)

사실 별거 없습니다. fork 누르고 Repository 이름을 `GitHub username.github.io` 설정하면 됩니다.
> 이름을 잘못 설정했다면, setting에 들어가서 다시 변경할 수 있습니다.

**끝**입니다. 간단하죠?

GitHub 잔디를 심고싶다면 [여기]()를 참고하세요.

## GitHub Pages 확인

Reposity에서 `Settings > Pages`에 들어가면 GitHub Pages 설정을 확인할 수 있습니다.  

보통 `main` 브랜치를 선택하고, 디렉토리는 `/ (root)`로 설정하면 자동으로 블로그가 배포됩니다.

`https://github username.github.io`로 접속해보면 블로그가 뜹니다.

>1 ~ 5분 정도의 시간이 걸립니다.

여기서 운명이 갈립니다.

![first_blog](/assets/img/github_pages/first_blog.png)

만약 고른 테마의 Demo와 같은 블로그가 개설이 되었다?

축하드립니다. 당신은 아래의 `기본 설정 변경하기` 챕터로 넘어가셔도 됩니다. 

아래의 내용을 몰라도 블로그를 작성하는데 아무런 문제가 없습니다.

![layout](/assets/img/github_pages/layout.png)

혹시 이런식으로 뜨셨나요? 

<del>축하드립니다. 당신은 저와 같은 깐깐한 입맛의 소유자입니다.</del>

github내에서 바로 빌드가 어려운 복잡한 테마의 경우 이런 식으로 뜬다고 합니다.

<del>따라하기 귀찮다면 그냥 간단한 테마로 새로 고르는 것도 추천드립니다</del>

##  Ruby 와 Jekyll 설치

제 포스팅은 `Chripy`테마로 블로그를 생성한 과정입니다.

>혹시 다른 테마를 선택하셨고, 제 포스팅을 참고했는데도 안된다면 당신의 친구 `chatGPT`한테 물어보세요.

`Chirpy`를 쓰려면 `Ruby`와 `Jekyll`을 설치하고 `Bundler`도 같이 깔아야 합니다.

### Ruby 설치

macOS에는 기본으로 탑재되어 있다고 하니, 다른 OS의 경우에만 설치해주시면 될거 같습니다.

[RubyInstaller 공식 사이트](https://rubyinstaller.org/)

`WITH DEVKIT` 버전을 다운하시면 됩니다.

설치하면서 `MSYS2` 옵션을 같이 설치하라고 뜨는데, 꼭 설치해야 합니다.

설치하는 과정 스크린샷을 못 찍었는데, 참고 이미지 없어도 잘 하실거라 믿습니다.

설치가 다 끝나고, 터미널(명령 프롬프트 혹은 Git Bash)을 열어서 아래의 코드를 각각 입력했을 때 버전이 나오면 성공입니다.

```bash
ruby -v

gem -v
```


### Jekyll & Bundler 설치

Ruby가 설치되면, 터미널(또는 Git Bash)를 열고

```bash
gem install jekyll bundler
```

설치 다 되는데 몇 분 정도 걸릴 수 있습니다

### 설치 이후 해야 할 것

git clone으로 블로그 Repository를 컴퓨터로 가져오세요.

>터미널에서 git clone하는 방법이나 GitHub Desktop을 사용해서 clone하는 방법중 편하신걸로 하세요

```bash
# 프로젝트 폴더로 이동
cd your-blog-repo

# 필요한 gem 설치
bundle install

# 로컬에서 사이트 띄우기
bundle exec jekyll serve
```

그럼 `http://localhost:4000` 에서 블로그를 볼 수 있습니다.

이때 에러없이 정상적으로 잘 뜬다면 GitHub Pages에도 정상 배포 가능한 상태입니다.

## GitHub Pages 배포하기

터미널에서 다시 프로젝트 폴더로 이동한 후 

```bash 
bundle exec jekyll build
```
를 입력한다면 `_site/` 폴더 안에 **정적 사이트 파일**이 생성이 됩니다.

이 `_site/`폴더가 **최종 배포용 파일** 입니다.

### GitHub에 gh-pages 브랜치 만들기

혹시 터미널을 닫거나 프로젝트 폴더를 벗어났다면, 다시 프로젝트 폴더로 이동해 줍니다.

터미널에 아래의 코드를 입력해줍니다.
```bash
git checkout --orphan gh-pages
git reset --hard
```

> `gh-pages`라는 비어있는 브랜치를 만드는 코드입니다.
>
> main source 코드들과는 섞이면 안되기 때문에 비어있는 orphan 브랜치를 사용합니다.

이제 `_site/`폴더 안으로 이동해 줍니다
```bash
cd _site
```

그 후 `.git`을 초기화 하고 
```bash
git init
git add .
git commit -m "Deploy my blog"
# who you are 이라고 뜬다면 그 아래의 git config로 뜨는 명령어 맨 뒤 "" 안의
# 내용만 수정해서 둘 다다실행 후 위의 명령어부터 다시 입력해주세요.
git branch -M gh-pages
git remote add origin https://github.com/내계정명/내저장소명.git
git push -f origin gh-pages
```
‼️ 주의: origin 주소는 당신의 GitHub 저장소 주소로 바꿔줘야 합니다.

>블로그 내용을 수정하고 재배포할때도 같은 코드를 입력하면 됩니다.

### GitHub Repository 설정 수정

GitHub Repository로 가서

Settings ➔ Pages 탭 들어가서

아래 이미지와 같이 설정해 준 후 `save` 버튼을 누르면 **끝**납니다

![Setting](/assets/img/github_pages/Settings_pages.png)

이제 조금만 기다리면 `https://내계정명.github.io/`주소로 블로그가 열립니다.


## 기본 설정 변경하기

블로그를 개인의 스타일로 바꾸기 위해 가장 먼저 수정해야 할 파일은 `_config.yml`입니다. 

사이트 이름, 이메일, 소개글, SNS 링크 등 여러 정보를 이 파일에서 바꿀 수 있습니다.

