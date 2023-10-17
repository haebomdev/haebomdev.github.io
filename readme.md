1. 모든 게시글은 category 폴더에 넣습니다
2. category 바로 아래 자식 폴더는 언어 이름으로 합니다
3. 새로운 카테고리 생성 시 아래 2가지를 필수로 생성합니다
   - `_post` 폴더: 이곳은 게시글(.markdown)이 담길 폴더입니다
   - index.html
     ```
     ---
     layout: list
     title: tool
     ---
     ```
4. 게시글 파일 이름의 규칙: `YYYY-MM-DD-이름.markdown`
   - 이름 내에 띄어쓰기가 필요할 시 `-`로 대체하여 지정하세요
5. 게시글의 메타데이터의 규칙을 지켜주세요 (모든 항목 생략 불가)
   ```
   ---
   layout: post
   title: "파이썬 기초"
   date: 2023-10-14 18:39:35 +0900
   author: KDH
   description: Python Fundamental
   thumbnail: https://www.w3schools.com/css/paris.jpg
   ---
   ```
   - `title`은 공백이 허용되니 `-`를 쓰지 맙시다
   - `date`는 원하는 게시 날짜로 맞춥시다 (날짜는 게시글 정렬용)
   - `author`에 자신의 이름 또는 닉네임을 적습니다
   - `description` 한 두 문장 정도로 요약한 내용을 적으세요
   - `thumbnail` 생략해도 되긴 합니다만 그러지 맙시다
