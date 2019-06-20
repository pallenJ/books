# Spring3

## Connection Pool

### Commons DBCP

- 데이터베이스와 애플리케이션을 효율적으로 연결하는 커넥션 풀(connection pool) 라이브러리.
- 잘 사용하면 데이터베이스와 애플리케이션의 일부분에서 발생하는 문제가 전체로 전파되지 않게 할 수 있고, 
일시적인 문제가 긴 시간 이어지지 않게 할 수 있음.
  + 뒤집어 말하면 적절치 못하게 값을 설정하여 어플리케이션의 값을 잘못 사용시 커넥션 풀이 APP의 병목지점이 될 수 도 있음
- 버전 선택은 jdk 버전에 따라 사용. 주요 버전과 그에 해당하는 jdk, jdbc 버전은 아래와 같음

     |Commons DBCP | JDK     | JDBC
     ------------  | ----    | -----
     |  2          | 7       | 4.1
     | 1.4         | 6       | 4
     | 1.3         | 1.4~1.5 | 3
- Connection.getMetaData() 메서드를 호출한 다음 커넥션을 닫지 않았을 때 메모리 누수가 발생하는 문제 등 주요 버그가 Commons DBCP 1.4.1에서 패치됐지만 몇 년째 Commons DBCP 1.4.1의 정식 배포는 나오지 않고 있음.
- Commons DBCP 2에는 Commons DBCP 1.4.1의 패치가 반영됐고 Commons DBCP 1.4.x보다는 비교적 활발히 개발이 이어지고 있음. jdk 7 버전부터 사용가능.
  > DBCP 1.4.1의 누수 버그에 대한 내용이 필요할시 https://issues.apache.org/jira/browse/DBCP-330 참고
  
  
