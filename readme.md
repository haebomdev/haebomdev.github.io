# Notice

## 1. 필수사항

1. 모든 게시글은 `category` 폴더에 저장
2. 폴더 및 파일 명명 규칙
   - "소문자 영문"
   - 띄어쓰기는 `-`로 대체하기
     - 단, 파일 내 상단 메타데이터의 `title`은 자유롭게 설정 가능
3. 작성 후 `main` 브랜치로 Pull Request

## 2. `category` 폴더 관리 규칙

```
category
├── index.html
├── en/
│   ├── tool/*
    │    ├── index.html
    │    └── _post/
│   └── help/*
└── kr/
    ├── tool/*
    │    ├── index.html
    │    └── _post/
    └── language/
        ├── fundamental/*
        │    ├── index.html
        │    └── _post/
        └── python/*
             ├── index.html
             └── _post/
```

1. `category` 폴더 바로 아래에...

   - 하위 폴더로는 언어별 구분된 폴더만 가능합니다
   - index.html에 모든 카테고리를 `<nav>` 안에 명시합니다

2. 새로운 카테고리 생성 시

   1. 생성할 카테고리가 말단 카테고리 폴더인지 확인합시다
      - 말단 카테고리 폴더: 위의 예에서 \*가 붙은 폴더
   2. 말단 카테고리 폴더\*일 경우, 아래 2가지는 필수로 생성하자!
      - `_post` 폴더: 이곳은 게시글(.markdown)이 담길 폴더입니다
      - index.html
        ```yaml
        ---
        layout: list
        title: tool  // 카테고리명과 "동일"하되 `-`은 공백으로 대체
        ---
        ```
   3. 카테고리 폴더(말단 제외) 바로 아래에 위의 2가지는 없도록 옮기거나 삭제하세요

## 3. 게시글 파일 작성 시

1.  파일 이름의 규칙: `YYYY-MM-DD-이름.markdown`
2.  각 말단 카테고리 폴더 별 게시글 수는 `15개 이하`
    - 초과 시 새로운 하위 카테고리를 생성하세요
3.  사진은 외부에 저장하고 이미지 주소 링크로만 게시글에 삽입해주세요
    - Google Drive, AWS S3 등 어느 곳이든 상관 없습니다
4.  게시글의 메타데이터의 규칙 (모든 항목 생략 불가)
    ```yaml
    ---
    layout: post
    title: "파이썬 기초"                      // "" 필수
    date: 2023-10-14 18:39:35 +0900
    authors: [lazybuttrying, Maple Syrup]    // 한 명이어도 배열로
    reviewers: [wow]                         // 한 명이어도 배열로
    description: "Python Fundamental"        // "" 필수
    thumbnail: https://www.w3schools.com/css/paris.jpg
    ---
    ```
    - `title`은 공백이 허용되니 `-`를 쓰지 맙시다
    - `date`는 원하는 게시 날짜로 맞춥시다 (날짜는 게시글 정렬용)
    - `author`에 자신의 이름 또는 닉네임을 적습니다 (검수자는 맨끝에)
    - `description` 한 두 문장 정도로 요약한 내용을 적으세요
      - 줄바꿈 지원 안 됩니다
    - 생략 가능한 항목이 있지만 그러지 맙시다
      - `thumbnail`
      - `reviewers`

## 4. 작성 TIP

1. `Obsidian`으로 마크다운 타입 게시글을 작성합니다: https://obsidian.md/download
   - `mermaid` 차트 렌더링도 지원합니다
   - 복사-붙여넣기 이미지를 자동으로 이미지 파일로 저장해줍니다
     - [주의]: Obsidian의 `설정` -> `파일 및 링크` -> `[[wikilink]] 사용` 해제하기
2. 참고글
   1. 마크다운 문법: category/kr/tool/2023/10/13/markdown-syntax.html
   2. 이미지 올리기: category/kr/language/2023/10/17/image-upload.html
