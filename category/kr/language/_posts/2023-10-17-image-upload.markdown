---
layout: post
title: "이미지 파일 업로드 후 마크다운에"
date: 2023-10-17 18:39:35 +0900
authors: [KDH, MapleSyrup]
description: "모두가 접근할 수 있는 퍼블릭 권한으로"
thumbnail: https://img.freepik.com/free-vector/images-concept-illustration_114360-298.jpg
---

먼저 마크다운에서 이미지를 올리는 방법에 대해 봅시다

이 글에서는 내가 가진 이미지를 `이미지 링크`로 가져오는 방법에 대해서 알아봅니다

```
// 순수
![설명](이미지 링크)

// HTML
<img src="이미지 링크" alt="설명" />

```

# Google Drive

1.  자신의 구글 계정 하에서 사진들을 구글 드라이브에 업로드 합니다.
2.  사진 하나하나 우클릭하여 `공유`->`일반 액세스: 링크가 있는 모든 사용자` -> `링크 복사`

    [모든 사진을 일일이 해줘야 하는 게 참 번거롭습니다]

3.  복사된 링크를 마크다운 파일 속 해당 이미지 위치의 `이미지 링크`에 대체합니다

    ```
    // Before
    ![설명](image_filename.png)

    // After
    ![설명](https://drive.google.com/file/d/1Fk0r5odYB00JqvdvVIxDuyuf2OjZuA_i/view?usp=share_link)
    ```

# AWS S3

1.  [처음에만] 버킷 생성 및 설정

    1. AWS S3 bucket을 `모든 퍼블릭 액세스 차단`을 허용하여 생성합니다
    2. 생성한 bucket을 클릭하여 `권한` -> `버킷 정책` -> `편집`에 아래 내용을 넣습니다
       - `{BUCKET_NAME}`에 자신의 bucket 이름으로 대체합니다
       - `변경 사항 저장` 필수
       ```json
       {
         "Version": "2012-10-17",
         "Statement": [
           {
             "Sid": "AddPerm",
             "Effect": "Allow",
             "Principal": "*",
             "Action": "s3:GetObject",
             "Resource": "arn:aws:s3:::public-haebom/*"
           }
         ]
       }
       ```

2.  이미지 업로드 및 링크 가져오기

    1. 사진들을 bucket에 업로드합니다
    2. 업로드된 사진을 클릭하여 `속성`-> `객체 개요` ->`객체 URL`을 복사합니다
    3. 복사된 링크를 마크다운 파일 속 해당 이미지 위치의 `이미지 링크`에 대체합니다

       ```
        // Before
        ![설명](Charts_in_Colaboratory_11_0.png)

        // After
        ![설명](https://public-haebom.s3.ap-northeast-2.amazonaws.com/library/Charts_in_Colaboratory_11_0.png)
       ```

3.  링크를 잘 보면 `파일 이름이 그대로` 남아 있습니다

    - 그렇기에 하나의 사진만 링크를 복사해오고
    - 그 이후로는 이미지 링크에서 파일명 외 부분을 복사-붙여넣기하면 됩니다

      ```
      https://public-haebom.s3.ap-northeast-2.amazonaws.com/library/
      ```
