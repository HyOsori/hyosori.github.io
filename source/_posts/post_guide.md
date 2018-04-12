---
title: 기술블로그 글쓰기 가이드
date: 2018-03-30 13:24:30
author: CameliaOvO
githublink: https://github.com/CameliaOvO
tags: [guide]
---

## Hexo를 몰라도 쓸 수 있는 글쓰기 가이드

1. 자기 레포로 Fork 떠가서 작업

1. `_post` 디렉토리에 `yyyy-mm-dd-title.md`로 게시글 작성 **title은 절대 겹치면 안돼요!**

1. 파일 상단에 `front-matter` 작성

```
---
title:             # 포스트의 제목을 작성해 주세요
date:              # 작성 일자 YYYY-MM-DD HH:MM:SS 형태로 작성해 주세요
author:            # 작성자 이름 혹은 깃허브 아이디
githublink:        # 작성자 깃허브 프로필 링크 (ex. https://github.com/CameliaOvO)
tags:              # 태그 목록 [태그1, 태그2, ... ] 가능하다면 영문소문자, 숫자, 하이픈으로만 ..
---
```

1. 작성된 글을 commit 후 PR 날려주세요! merge되면 자동으로 빌드해서 게시글이 올라갑니다.


## 추가 팁

1. 이미지 파일은 `source/images`에 업로드 후 `/images/imageName.png`와 같이 사용하시면 됩니다.
1. 디자인 센스가 극악이라 저게 최선이었습니다. 디자인 변경 PR **언제든지 환영합니다.**
