# AGENTS.md

## Project

이 프로젝트는 AI Agent가 기능을 구현하고 자동화된 검증을 수행할 수 있도록 설계된 Spring Boot Backend 프로젝트다.

## Before Starting Work

작업을 시작하기 전에:

1. 현재 프로젝트 구조를 확인한다.
2. 이 파일의 규칙을 확인한다.
3. 현재 작업과 관련된 요구사항을 확인한다.
4. 관련된 architecture 및 constraints를 확인한다.
5. 기존 코드와 테스트를 확인한다.

프로젝트 전체 파일을 무차별적으로 읽지 않는다.
현재 작업과 관련된 영역을 탐색하여 필요한 컨텍스트를 확보한다.

## Implementation

* 요구사항에 없는 기능을 임의로 추가하지 않는다.
* 기존 코드와 구조를 먼저 이해한 후 수정한다.
* 기존 구현과 일관된 방식을 우선한다.
* 구현 방법을 결정하기 전에 관련 코드를 탐색한다.

## Database

* Schema 변경은 Flyway Migration으로 수행한다.
* 기존 Migration을 수정하지 않는다.
* Schema 변경이 필요한 경우 새로운 Migration을 추가한다.
* Hibernate의 자동 Schema 변경에 의존하지 않는다.

## Testing

구현 후 관련 테스트를 실행한다.

최소한 다음을 확인한다.

* Compile
* Relevant Tests

테스트가 실패하면 실패 원인을 분석하고 수정한 후 다시 검증한다.

## Completion

작업을 완료했다고 판단하기 전에:

* 요구사항을 만족하는지 확인한다.
* 관련 테스트가 통과하는지 확인한다.
* 변경된 파일을 확인한다.
* 불필요한 변경이 포함되지 않았는지 확인한다.
