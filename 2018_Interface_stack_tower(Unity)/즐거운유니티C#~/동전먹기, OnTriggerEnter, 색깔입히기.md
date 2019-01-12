### 동전먹기
> 'Is Trigger' 체크로 오브젝트가 동전에 닿자마자 반응하게 함
```c#
//class는 Coin
void OnTriggerEnter(Collider c)
{
 if(c.gameObject.name == "Ball")
 {
   Destroy(gameObject); // 여기서gameObject는 class와 일치하는 Coin 말하는거임.
                        // Coin을 없애라~
 }
}
```

### 색깔 입히기
> 프로젝트 뷰-> new material 생성 -> 인스펙터 창 'Main Maps' -> 색깔 조정  
-> 색 입힐 오브젝트에 드래그&드랍
