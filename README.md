# [크래프톤 정글] Bob Friend

기간: 2022년 10월 25일 → 2022년 10월 27일
태그: Github, Javascript, MongoDB, Python, Team Project

## Overview

---

크래프톤 정글 1기 입소생들의 빠른 친목도모를 위해 같이 밥 먹을 사람을 구할 수 있는 주제로 프로젝트를 진행하였습니다.

사용자는 새로 모임을 등록하거나, 기존 모임에 참여 할 수 있으며 모임에 참여하는 사람의 닉네임만을 제공하여 누구랑 먹을 지 모르는 긴장감을 통해 재미를 제공합니다.

## Goal

---

**-기술 구현 목표** 

- 로그인 기능
- jinja2를 이용한 서버사이드 렌더링
- JWT 인증 방식 사용
- 정규화를 활용한 회원가입 입력 폼 체크
- tailwind 활용

**-회원관리 기능 개발**

1. 회원가입
2. 로그인
3. 로그아웃
4. 회원정보 변경

**-밥친구 찾기 기능 개발**

1. 모임 개설
2. 모임 조회
3. 모임 참가
4. 모임 확정
5. 모임 삭제

## Tech Stack

---
![Untitled](https://github.com/JeonJe/Bobfriend/assets/43032391/0ed46e5b-4a45-4f11-b803-0ee6754c92df)
- Front-End : Javascript, Tailwind, Ajax, Jquery
- Back-end : Python flask
- Database : MongoDB
- Tools : Trello, Slack, Github

## Role

---

- 프로젝트 기획, 설계, 개발
- 회원가입 기능 개발
    - 정규식을 사용하여 회원가입 데이터 유효성 검사 (클라이언트사이드, 서버 사이드)
    - Ajax를 사용하여 중복 체크 및 회원가입 데이터 저장
- 모임 카드 삭제 배치 작성
- 모임 참여,취소 기능 개발
- 다른 팀원 트러블 슈팅 팔로우 
    
    

## 개발 화면

---


![1](https://user-images.githubusercontent.com/43032391/229364050-d9b3ea21-e0e8-4e8a-b343-1d46c5075757.png)
![2](https://user-images.githubusercontent.com/43032391/229364065-b3c47e9f-6e81-451e-8939-79e933f23280.png)
![3](https://user-images.githubusercontent.com/43032391/229364084-774114bb-b094-4b94-9ccd-fc7d24e63f14.png)


## Takeaway

---
- 모임 카드를 생성할 때, 현재 시간보다 과거 시간으로 예약하지 못하도록 예외처리하는 로직을 구현하였습니다. 로컬 테스트까지 정상적으로 완료하였으나 AWS EC2에 배포 시 모임 예약이 되는 문제가 발생하였습니다.
    
    로컬 개발환경과 서버와의 다른 점을 확인하는 방향으로 문제 해결을 접근한 결과 AWS EC2은 instance의 생성 시 기본적으로 Timezone이 UTC(세계 표준시)를 사용한 다는 것을 알게 되었습니다.
    
    EC2 서버 시간을 한국 시각으로 변경하니 정상적으로 동작하는 것 확인하였고, 실제 서버에 배포할 때 시간을 사용한다면 Server Time Zone도 고려 해야한다는 것을 알게 되었습니다.
    
- Github 사용 관련해서 부족한 점이 많다는 것을 깨달았습니다.
- 세션과 다른 JWT 을 활용한 인증방식의 장단점 배울 수 있었습니다.

## **느낀점**

---

- 처음 만난 정글 동기와 3박 4일 미니 프로젝트를 진행하면서 개발에 열정적이고, 잘하는 사람이 많다는 것을 느꼈습니다.
- tailwind CSS와 최근 트렌드의 프론트엔드 프레임워크을 사용하면서 프레임워크의 효율성에 대해 놀랐습니다. tailwind는 HTML 내 class 태그에 어떤 것을 쓸지만 추가하면 자동 스타일링이 되어 스타일을 하나씩 찾아야 하는 번거로움을 줄일 수 있었습니다

## Etc

---

- 프로젝트 관리(트렐로) : [https://trello.com/b/yVU1UAUz/week00-mini-project](https://trello.com/b/yVU1UAUz/week00-mini-project)
