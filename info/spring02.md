# spring2

## Lombok

- 자바 컴파일 시점에서 특정 어노테이션으로 해당 코드를 추가할 수 있는 라이브러리. 이는 코드의 간결화로 가독 성 및 유지 보수에 많은 도움이 됨.
- 자주 사용되는 어노테이션
  + @Getter, @Setter, @ToString : 해당 어노테이션과 동일한 이름의 메소드 자동 생성. 필드 변수위에 사용시 해당 변수에 대해서만 메소드 생성.
  + @NoArgsConstructor : 파라미터가 없는 기본 생성자 생성
  + @AllArgsConstructor : 모든 필드값을 파라미터로 받는 생성자 생성
  + @EqualsAndHashCode : equals 와 hashCode 메소드 자동생성
  + @Data :  @ToString, @EqualsAndHashCode, @Getter, @Setter, @RequiredArgsConstructor 등 VO에 쓰이는 어노테이션을 자동 수행
  
- 주의사항
  + @Data는 강력한 어노테이션이나 남발시 보안적인 문제가 생길 수 있음.
