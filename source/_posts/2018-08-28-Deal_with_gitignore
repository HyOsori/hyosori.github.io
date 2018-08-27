---
title: .gitignore 다루기
date: 2018-08-28 01:59:48   # 작성 일자 YYYY-MM-DD HH:MM:SS 형태로 작성해 주세요
author: CameliaOvO           # 작성자 이름 혹은 깃허브 아이디
githublink: https://github.com/cameliaOvO       # 작성자 깃허브 프로필 링크 (ex. https://github.com/CameliaOvO)
tags: [git]             # 태그 목록 [태그1, 태그2, ... ] 가능하다면 영문소문자, 숫자, 하이픈으로만 ..
---

 git으로 협업을 하다보면 **이건 공유할 필요가 없는데....** 라던가 **이건 공유하면 안되는데?!** 같은 파일이나 폴더들이 종종 생깁니다. 예를 들자면 ..


#### 이건 공유할 필요가 없는데...
.DS_Store (macOS에서 폴더 메타데이터를 저장하는 파일)
.idea (Jetbrain사에서 만든 IntelliJ라던가 PyCharm과 같은 IDE의 옵션 폴더)
__pycache__ , .pyc, .pyo ... (미리 컴파일된 파이썬 코드)
venv (파이썬 가상환경)
거대하고 어마어마한 양의 input이나 로그 데이터 (물론 팀끼리는 공유해야 하지만 굳이 git으로 ...?)

#### 이건 공유하면 안되는데?!
각종 api 토큰
dbconfig같은 파일에 들어있을법한 db접근 정보 + (혹은 root 비밀번호 ..!!)
웹 스크래핑 등에 사용하기 위한 개발자 개인의 token, id / password ~~(이건 진짜 큰일인데 깃헙 돌아다니다보면 여럿 보여요ㅎㅎ 다 재발급 받았겠지요..)~~


 `.gitignore` 파일을 만들고 그 안에 공유하고 싶지 않은 파일들에 대한 패턴을 적으면 저런 파일들을 무시할 수 있습니다.

갓 `git-scm`의 예를 가져오자면 ..

```bash
$ cat .gitignore
*.[oa]
*~
 ```

 (cat 명령어는 모두 알 거라 믿고) 첫번째 줄은 `.o` 나 `.a`로 끝나는 파일을 Git이 무시하라는 것이고 두번째 줄은 ~로 끝나는 모든 파일을 무시하라는 것입니다. (.o나 .a는 내가 작성한 파일이 아니라 빌드할 때 생성되는 파일들이고, ~로 끝나는 애들은 vim같은데서 쓰다가 만 파일들? 입니다.)

 저런 것 말고도 위에서 적은 환경, 실행파일 등의 항목들도 아래 규칙에 따라서 추가할 수 있습니다. (from. git-scm)

* 아무것도 없는 줄이나, #로 시작하는 줄은 무시한다.
* 표준 [Glob](https://en.wikipedia.org/wiki/Glob_(programming) 패턴을 사용한다. (Glob에 대한 설명은 링크 참조)
* 디렉토리는 슬래시(/)를 끝에 사용하는 것으로 표현한다.
* 느낌표(!)로 시작하는 패턴의 파일은 무시하지 않는다.

#### 또 다른 예시
```bash
# ignore all .a files
*.a

# but do track lib.a, even though you're ignoring .a files above
!lib.a

# only ignore the TODO file in the current directory, not subdir/TODO
/TODO

# ignore all files in the build/ directory
build/

# ignore doc/notes.txt, but not doc/server/arch.txt
doc/*.txt

# ignore all .pdf files in the doc/ directory and any of its subdirectories
doc/**/*.pdf
```

기왕이면 프로젝트 처음 만들 때 먼저 만들어 두는 것을 추천해요. (커밋한 뒤 rebase로 되돌리는 것까지는 몰라도 커밋하고 푸쉬한 뒤 되돌리려면...)

[커밋하고 푸쉬까지 해버렸는데 되돌리고 싶다면 이 게시글을 참고하세요](https://cameliaovo.github.io/2018/02/27/Removing-sensitive-data-from-a-repository/)


#### 어떤 내용을 추가해야하는지 감이 안잡히거나 일일히 추가하기 귀찮다면 
1. [gitignore.io](https://www.gitignore.io/)라는 사이트인데 여기서 자기 개발환경, 언어를 적으면 쉽게 기본적인 `.gitignore`에 들어갈 내용을 만들 수 있어요.

1. [github/gitignore](https://github.com/github/gitignore)에서도 언어, 환경, 프레임워크 등에 따라  `.gitignore`에 어떤 내용이 들어가야하는지를 쉽게 복붙할 수 있어요. (참고로 이 파일들은 github에서 레포지토리 처음 생성할때 추가하는 gitignore에 있는 그 파일들이에요)

### reference

git-scm : https://git-scm.com/book/en/v2/Git-Basics-Recording-Changes-to-the-Repository#_ignoring
동일한 글이 [여기](https://cameliaovo.github.io/2018/08/27/Deal-with-gitignore/)에도 있습니다.
