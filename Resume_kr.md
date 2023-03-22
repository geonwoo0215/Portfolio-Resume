## 이건우

### 기본정보
- 이메일: gw980215@naver.com
- Github: https://github.com/geonwoo0215
- blog: https://dailydebug.tistory.com/


### 학력
상명대학교, 게임학과
2017.03 ~  
현재 졸업유예

### 보유 기술
- 백엔드
  - JAVA 17
  - SpringBoot, Spring data JPA
  - MySQL : 쿼리 작성 및 인덱스 활용 가능

## 프로젝트

### KKINI

#### 소개
- KKINI는 동네에서 밥 친구를 만들고 싶은 사람, 혼자 가기 힘든 음식점을 가고 싶은 사람, 나만의 맛집을 공유하고 싶은 사람들이 모임을 결성하고 참여할 수 있는 서비스입니다.

#### 개발 환경
- JDK 17, Gralde 7.6, Spring Boot 2.7.8, MySQL, Spring Data JPA, Spring Sercurity, Redis, flyway, Amazon aws, mapstruct, Lombok, Spring Bean Validation

#### 데이터베이스 설계 원칙
- Where 조건에 들어가는 컬럼들을 INDEX를 생성
- 공통 칼럼(created_at, updated_at, deleted)
- 스키마 변경은 flyway로 버전 관리
- row 삭제는 소프트 삭제 처리
- PK는 auto_increment를 사용하여 Mysql이 따로 정렬하지 않도록 설정


#### 주요 기능 및 구현사항 소개

1) 모임 생성
- 사용자가 모임을 생성하였을 때 모임을 생성하고 사용자를 방장으로 만듬
  - 메서드가 두 가지 책임을 지지 않게 하기 위해 EventListener를 활용하여 책임 분리
  - 매핑 코드가 비즈니스 코드와 혼합되어 가독성이 떨어지는 것을 방지하기 위해 mapStruct 사용

2) 모임 조회
- 오프셋 기반 페이지 네이션을 사용하여 구현
- 오프셋 기반 페이지 네이션의 성능 문제를 고려하여 커서 기반 페이지 네이션으로 변경하고 커서를 id로 지정하여 인덱스 활용

3) 사용자 위치 기반 범위 검색
- 사용자를 기준으로 반경 500m 이내의 모임을 조회
- MySQL 공간 함수를 사용하여 위경도 거리 계산, 공간 인덱스를 활용하여 성능 최적화

#### 교육

#### 교육과정

#### 링크 :[백엔드 데브코스](https://school.programmers.co.kr/learn/courses/16622/16622-4%EA%B8%B0-k-digital-training-%ED%81%B4%EB%9D%BC%EC%9A%B0%EB%93%9C-%EA%B8%B0%EB%B0%98-%EB%B0%B1%EC%97%94%EB%93%9C-%EC%97%94%EC%A7%80%EB%8B%88%EC%96%B4%EB%A7%81)

#### 스터디

2022.10 ~ 2022.11 디자인 패턴 스터디(5명)
- 디자인 패턴을 학습하여 객체지향적인 코딩을 작성을 고민하고, 스프링이 어떠한 디자인 패턴을 활용했는지 학습
- 싱글톤, 프록시, 어뎁터, 데코레이터, 팩토리, 템플릿 메서드 패턴 학습
- 모두가 주제에 대해 자료 준비, 발표 당일 랜덤
- 발표 전에 노션과 깃허브로 발표 내용 정리 
  
##### 깃허브 링크 [디자인 패턴 스터디](https://github.com/Pre-FTeam/design-pattern)

2022.11 ~ 2023.01 면접을 위한 CS 전공지식 노트 책 스터디 (5명)
- CS에 대한 기초적인 지식이 부족하여 학습
- 네트워크, 운영체제, 데이터베이스, 자료구조 학습
- 책이 모든 내용을 담지 않고 추상적으로 설명하여 구체적으로 따로 조사, 학습 진행
  - 발표자는 매일 랜덤으로 월 ~ 금 각자 한 명씩 정하여 지정된 범위를 학습하고 발표
  
##### 깃허브 링크 [면접을 위한 CS 전공지식 노트 책 스터디](https://github.com/prgrms-web-devcourse/Team-BlackDog-CS-Book-Study) 
