# Architecture

## 1. General

* Backend application은 Spring Boot 기반으로 구성한다.
* 애플리케이션은 계층형 구조를 기본으로 한다.
* 비즈니스 로직은 Controller에 두지 않는다.
* 데이터베이스 접근은 Repository 계층을 통해 수행한다.

## 2. Layers

### Controller

* HTTP 요청과 응답을 처리한다.
* 비즈니스 로직을 직접 수행하지 않는다.
* 모든 데이터는 요청 데이터는 DTO 파일로 대체한다.

### Service

* 비즈니스 로직을 담당한다.
* 트랜잭션 경계를 관리한다.

### Repository

* 데이터베이스 접근을 담당한다.

### Domain

* 핵심 비즈니스 데이터를 표현한다.
* 각 도메인의 조회 및 변경 등 도메인 관련 기능 로직은 도메인 내부에 작성한다.

## 3. Dependency Direction

* 의존성은 가능한 한 다음 방향을 따른다. Controller → Service → Repository
* Controller가 Repository를 직접 호출하지 않는다.


## 4. Authentication

* Spring Security 를 사용한다.
* 인증 방식은 JWT 기반으로 AccessToken 과 RefreshToken 을 사용한다.