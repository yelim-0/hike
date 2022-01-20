# 서지정보 작성하기

현재의 디렉토리(/content/publications)에 아래의 정보를 작성해주세요. 파일 생성시 yaml 확장자로 생성하세요. 논문 인용 방법은 IEEE를 따릅니다.

- 파일제목은 [유형]제목3-4단어.yaml로 생성합니다.

유형: IJ(International Journals), DJ(Domestic Journals), IC(International Conferences), DC(Domestic Conferences), W(Workshops), B(Book Chapters), P(Posters)를 사용해주세요.

제목 형식: CamelCase로 작성합니다.

예시: [IJ]ACombinationalMethodToDetermining.yaml

- classification: 카테고리 Journals(International Journals), Domestic Journals, Conferences(International Conferences), Domestic Conferences, Workshops, Book Chapters, Posters 중 선택하여 작성
- publishedDate: 출판된 연도와 월, 일 작성. 형식은 yyyy. mm. dd. 로 작성
- title: 제목
- subtitle: 국내 논문 또는 컨퍼런스의 경우, 제목의 영문명 작성
- author: 저자(풀네임으로 작성, 미들 네임의 경우 한글자로 줄임 가능)
- description: 서지 정보 작성
- link: 출판된 서지의 링크

```[yaml]
classification: Conferences
publishedDate: 2007. 11. 02-05.
title: A Combinational Method to Determining Identical Entities from Heterogeneous Knowledge Graphs 
author: Haklae Kim
description: Journal of Information Science Theory and Practice, vol. 6, no. 3, pp. 6–15, Sep. 2018.
link: https://ieeexplore.ieee.org/abstract/document/4407341
```
