# find() 와 getReference() 의 ㅊ이

---

## find() method

* EntityManager 의 Session 이 유지되는 상태에서 조회가능
* Session 이 끊어지면 다시 Transaction 획득 후 조회해야 함

## getReference() method

* 조회하고자 하는 Entity 의 Proxy 객체를 생성하여 반환
* Session 이 끊어진 이후에도 조회한 data 에 접근가능
* Session 이 유지된 상태에서 적어도 한 번 조회를 통해 Entity Proxy 객체가 data 를 가지도록 해야 함. 그렇지 않으면 EntityNotFoundException 발생
* lazy loading 기능을 제공