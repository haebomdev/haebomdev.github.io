---
layout: post
title: "Jupyter notebook to markdown"
date: 2023-10-13 18:39:35 +0900
author: KDH
description: Convert ipynb to md
thumbnail: https://img.freepik.com/free-vector/app-development-concept-with-desk-desktop_23-2148699345.jpg?w=996&t=st=1697547195~exp=1697547795~hmac=57b8d06f1f5e90e72837915688ae073cdee7e82445c7d0f2ac44315cd43a140e
---

노트북 파일을 마크다운 파일로 변환해주는 프로그램을 설치합니다.

```sh
pip install nbconvert
```

파일 이름과 마크다운 형식임을 표기하여 변환합니다.
명령어를 실행한 곳에서 NOTEBOOK_FILE.md 파일이 생성됩니다.

```
python -m nbconvert --to markdown NOTEBOOK_FILE.ipynb
```

출력 결과에 사진(그래프)가 있는 경우
결과 파일과 더불어 사진들이 저장된 폴더가 생성되며
그 폴더 이름 또한 NOTEBOOK_FILE입니다.

이 사진들을 마크다운 결과 파일과 함께 이동시켜야만 이미지를 확인할 수 있습니다.
