# Engineering Constraints

## 1. General

* 기존 코드를 수정할 때 기존 동작을 불필요하게 변경하지 않는다.
* 요구사항에 명시되지 않은 기능을 임의로 추가하지 않는다.
* 기존 아키텍처를 변경할 필요가 있다면 그 이유를 먼저 확인한다.
* Lombok 으로 대체할 수 있는 코드는 대체한다.
* `src/main/resources/application.properties`는 절대 수정하지 않는다.
* 테스트를 위한 설정은 `src/test/resources`의 테스트 전용 설정 또는 Spring Test Profile을 사용한다.
* 테스트 목적의 설정을 추가하기 위해 `src/main/resources`의 애플리케이션 설정을 변경하지 않는다.

## 2. Database

* 애플리케이션의 기본 Database는 PostgreSQL이다.
* Database Schema 변경은 Flyway Migration을 통해 수행한다.
* 기존 Flyway Migration 파일은 수정하지 않는다.
* 새로운 Schema 변경은 새로운 Migration 파일로 추가한다.
* JPA/Hibernate를 이용해 운영 Database Schema를 자동 생성하거나 변경하지 않는다.

## 3. Security

* 비밀번호는 평문으로 저장하지 않는다.
* 비밀번호 또는 인증 정보를 로그에 출력하지 않는다.
* 토큰에 비밀번호 등 민감정보를 포함하지 않는다.
* 인증정보를 로그에 출력하지 않는다.

## 4. Testing

* 새로운 기능에는 관련 테스트를 추가한다.
* 구현 완료를 테스트 통과 여부로 검증한다.
* 테스트가 실패한 상태에서 기능 구현을 완료했다고 판단하지 않는다.

## 5. Validation

기능 구현 후 가능한 범위에서 다음을 검증한다.

1. 컴파일
2. 단위 테스트
3. 통합 테스트
4. 관련 정적 검증
