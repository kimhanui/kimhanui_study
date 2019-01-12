### Collision 변수?
> 스크립트 작성 중인 오브젝트를 기준으로, 오브젝트에 충돌한 물체 감지

### 충돌 감지 메소드  
> 유니티에서는 충돌이 일어나면 특정 메소드(OnCollisionEnter( 충돌한 상대 ))를 호출   

예시)
```c#
void OnCollisionEnter( Collision a ) //a가 충돌한 물체
{
 Debug.Log(a.gameObject.name); //a의 이름 콘솔에 찍는다.
}
```

### Collision 변수 응용
```c#
void OnCollisionEnter( Collision a )
{
 Vector3 direction = transform.position - 
a.gameObject.transform.position;
 
 //direction 은 방향과 크기를 가진 '힘'으로 생각
 //direction.normalized는 direction의 크기를 1로 정규화 시킨것!
 direction = direction.normalized * 1000; // 곧 크기가 1000임.
 
 // 구한 방향으로 힘을 주자! AddForce(direction)
 a.gameObject.GetComponent<Rigidbody>().AddForce(direction);
}
```

### 충돌은 Collider가 하는거임
Collider끼리 부딪혔을 때 OnCollisionEnter가 호출
>  그래서 복잡한 캐릭터의 경우 Collider라도 단순화해서 씀


### rigidbody끼리 튕김/밀림 현상 방지  
```c#
 private void OnCollisionEnter(Collision collision)
    {
        if (collision.gameObject.tag == "Bird")
            collision.gameObject.GetComponent<Rigidbody>().isKinematic = true;
    //서로 닿았을 때 밀림 방지
    }
```

