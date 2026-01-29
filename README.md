# Spring Boot & JPA Board Project

본 프로젝트는 **Spring Data JPA**를 핵심 기술로 활용하여 구축한 객체지향 기반의 웹 게시판입니다. 기존의 SQL 중심 설계에서 벗어나 엔티티 중심의 도메인 설계를 통해 데이터베이스를 효율적으로 관리하는 데 중점을 두었습니다.

## 핵심 기술 스택
* **Backend**: Java 17, Spring Boot 5.0
* **Data Access**: **Spring Data JPA**, Hibernate
* **Database**: Oracle DB
* **Frontend**: JSP (Custom Red & White Design)
* **Library**: Lombok, Spring Web

---

## JPA 활용 핵심 포인트

### 1. 객체지향적 도메인 설계 (Entity)
* `@Entity` 및 JPA 어노테이션을 사용하여 자바 객체와 데이터베이스 테이블을 1:1로 매핑했습니다.
* 객체지향적인 관점에서 도메인을 설계하고 관리합니다.

### 2. Spring Data JPA Repository 활용
* `JpaRepository` 인터페이스를 상속받아 공통 CRUD를 자동화했습니다.
* **Query Method** 규칙을 활용하여 별도의 SQL 작성 없이 검색 기능을 구현했습니다.
  - `findByTitleContaining()`: 제목 기반 검색
  - `findByContentContaining()`: 내용 기반 검색
  - `findByWriterContaining()`: 작성자 기반 검색
* `@Query` 어노테이션을 통한 커스텀 JPQL 작성을 지원합니다.



### 3. 영속성 관리 및 데이터 처리
* `@Transactional`을 통한 서비스 계층의 트랜잭션 보장.
* **변경 감지(Dirty Checking)** 기능을 활용한 엔티티 업데이트 최적화.

---

## 주요 기능

### 📋 게시판 (Board)
* **게시글 CRUD**: JPA 엔티티 매핑을 통한 게시글 작성, 조회, 수정, 삭제.
* **통합 검색**: 제목, 내용, 작성자 등 다양한 조건의 검색 기능.

---

## Design Concept
* **Point Color**: `Red` (#ff0000)
* **Background**: `White`
* **Font Color**: `#151515`
* **Animation**: 버튼 호버 시 위로 이동 및 색상 반전 효과 적용.
