# 친그라운드 (CHINGROUND)

#### - 친구를 만나는 운동장, 친구+그라운드

#### - 제주창조경제혁신센터 SW개발자양성과정(3기), LIKELION in JEJU

## 제작

#### 이승수(제주대학교), 김범준(제주대학교), 송재용(연세대학교)

#### 기초 환경: Ruby on Rails 5.2, ruby 2.4.1, Ubuntu 16.04 LTS

## 목차

1. 서비스 소개
   1. 기초 기능 소개
   2. UI/UX 편의 소개
2. 서비스 이용 예시
   1. 모임기능
   2. 채팅기능
   3. 별점기능
   4. 프로필관리기능(유저 메뉴바 등)
   5. 알림기능 및 검색기능
3. 서비스 코드 설명
   1. 서비스용 기초 gem 목록
   2. 모임기능 코드
      1. DB구조
      2. 모임기능 예외처리
   3. 채팅기능 코드 (ActionCable)
      1. ActionCable 기초 이용
      2. 스크립트와 쿠키를 이용한 게시글과 유저와 관계 형성
   4. 별점기능
      1. 자체 평가 기준 수립
      2. 별점기능 예외처리
   5. 프로필관리기능
      1. 프로필 사진 설정
      2. 자신의 참여하고 있는 모임 및 채팅 요약
   6. 알림기능 및 검색기능
      1. 알림기능 구현: `gem 'unread'`
      2. 검색기능 구현: `gem 'ransack'`
4. 기타 추후 개선점
   1. 기능 상 개선점
   2. UI/UX 개선점
   3. 성능 최적화 개선점



## 1. 서비스 소개

### 1.1. 기초 기능 소개

기초 커뮤니티 서비스를 통한 다른 사람들과의 새로운 만남과 커뮤니티 활동 지원

![main](./info_pic/main.png)

### 1.2. UI/UX 편의 소개

![user-main](./info_pic/user-main.png)

![login](./info_pic/login.png)

## 2. 서비스 이용 예시 

### 2.1. 모임기능

모임기능에는 장소 및 일시 등을 넣을 수 있어 커뮤니티 활동 지원

![article-index](./info_pic/article-index.png)

![article](./info_pic/article.png)

### 2.2. 채팅기능

rails 5.2부터 탑재된 ActionCable을 활용하여 자유 채팅 및 게시물 채팅 지원

![chat_noti](./info_pic/chat_noti.png)

### 2.3. 별점기능

커뮤니티 활동 시 사용자간 충돌 및 위험성을 방지하기 위해 별점기능 탑재

![rating](./info_pic/rating.png)

### 2.4. 프로필관리기능(유저 메뉴바 등)

유저 메뉴바가 항상 존재하여 편하게 자신의 참가 내역 등 조회가능

마이페이지에서 자기 관리 가능

프로필 기능을 통해 친구와 팔로우/워 관계 맺을 수 있으며 이에 따른 알림기능 존재

![user-main](./info_pic/user-main.png)

![mypage](./info_pic/mypage.png)

![my-profile](./info_pic/my-profile.png)

### 2.5. 알림기능 및 검색기능

알림기능을 통해 게시물 신규 참가/미참가 알림, 댓글 알림, 채팅 알림 등을 받을 수 있음

(팔로우 한 사람에 관련한 알림 수신 가능)

검색기능으로 게시물, 친구 등 찾기 가능

![chat_noti](./info_pic/chat_noti.png)

![find-article](./info_pic/find-article.png)

![find-friend](./info_pic/find-friend.png)



## 3. 서비스 코드 설명

### 3.1. 서비스용 기초 gem 목록

```ruby
# aws-ses
gem 'aws-ses'

#rails db visualize
gem 'rails_db'
#authentication
gem 'devise' 

#jquery & bootstrap
gem 'jquery-rails'
gem 'bootstrap'

#serch engine
gem 'ransack'

#notice helper
gem 'unread'

# actioncable redis
gem 'redis'
```



### 3.2. 모임기능 코드

#### 3.2.1 DB구조

#### 3.2.2. 모임기능 예외처리



### 3.3. 채팅기능 코드 (ActionCable)

#### 3.3.1. ActionCable 기초 이용

#### 3.3.2. 스크립트와 쿠키를 이용한 게시글과 유저와 관계 형성



### 3.4. 별점기능

#### 3.4.1. 자체 평가 기준 수립

#### 3.4.2. 별점기능 예외처리



### 3.5. 프로필관리기능

#### 3.5.1. 프로필 사진 설정

#### 3.5.2. 자신의 참여하고 있는 모임 및 채팅 요약



### 3.6. 알림기능 및 검색기능

#### 3.6.1. 알림기능 구현: `gem 'unread'`

#### 3.6.2. 검색기능 구현: `gem 'ransack'`



## 4. 기타 추후 개선점

### 4.1. 기능 상 개선점

기능 상 커뮤니티의 활성화를 위한 다양한 재미있는 요소 추가

### 4.2. UI/UX 개선점

JS 추가를 통해 개선, AJAX를 통한 개선

### 4.3. 성능 최적화 개선점

DB구조 개선 및 리팩토링을 통한 비효율적인 코드 개선