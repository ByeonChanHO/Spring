# ACID

> ## [ 정의 ]
> 
>> ACID는 데이터베이스 트랜잭션이 안전하게 수행된다는 것을 보장하기 위해 지켜야할 성질을 가르키는 약어이다
>> 
>> A : Atomicity(원자성)
>> 
>> C : Consistency(일관성)
>> 
>> I : Isolation(독립성)
>> 
>> D : Durability (지속성)
>>
>> ### [ 트랜잭션 ]
>> 
>> 데이터베이스에서 데이터에 대한 하나의 논리적 실행단계를 트랜잭션이라고 한다.
>> 
>> 예를 들어, 은행에서 계좌이체를 트랜잭션이라고 할 수 있는데, 계좌 이체 자체를 구현은 내부적으로 여러단계가 있지만 전체적으로는 '송신자 계좌의 금액 감소', '수신자의 계좌의 금액 증가'가 한 동작으로 이루어져야한다.
>> 
>> ### [ 원자성 (Atomicity) ]
>>> 트랜잭션과 관련된 작업들이 부분적으로 실행되다가 중단되지 않는 것을 보장하는 능력
>>> 
>>> 예를 들어, 자금 이체가 이루어질때 **계좌에 돈이 입금 되는 건 성공되어도 이체한 계좌에서는 돈이 빠져나가는 건 실패해서는 안된다.**
>>> 
>> ### [ 일관성 (Consistency) ]
>>> 트랜잭션이 실행을 성공적으로 완료하면 언제나 일관성 있는 데이터베이스 상태를 유지한다는 의미이다
>>> 
>>> 예를 들어, [무결성 제약](https://github.com/ByeonChanHO/Back_End_Study/tree/main/%EA%B3%B5%EB%B6%80%EB%B0%A9/Event%20Driven)이 계좌는 잔고가 있어야 된다면, 이를 위반하는 트랜잭션은 중단되게 만든다.
>>> 
>> ### [ 독립성 (Isolation) ]
>>> 트랜잭션을 수행 시 다른 트랜잭션의 연산 작업이 끼어들지 못하도록 보장한다.
>>> 
>>> 즉, 트랜잭션은 실행은 연속적이어야하며 밖에 있는 어떤 연산도 중간 단계의 데이터를 볼 수 없음을 의미한다.
>>> 
>>> 예를 들어, 두사람이 하나의 계좌에 입금할시 한사람의 입금이 끝나고 다른 사람의 입금이 수행되어야 한다는 것이다.
>>> 
>> ### [ 지속성 (Durability) ]
>>> 성공적으로 수행된 트랜잭션은 수행되면 그 결과는 완전히 반영되어야 한다.
>>> 
>>> 예를 들어, 트랜잭션이 성공적으로 수행되면 로그를 남겨 예상치 못한 일로 인해 백업을 할 수 있게 해야한다.


## 참조
https://ko.wikipedia.org/wiki/ACID#:~:text=ACID(%EC%9B%90%EC%9E%90%EC%84%B1%2C%20%EC%9D%BC%EA%B4%80%EC%84%B1%2C,%ED%95%98%EB%8A%94%20%EA%B8%B0%EC%88%A0%EC%9D%84%20%EA%B0%9C%EB%B0%9C%ED%95%B4%20%EB%83%88%EB%8B%A4.
아직 미완성
