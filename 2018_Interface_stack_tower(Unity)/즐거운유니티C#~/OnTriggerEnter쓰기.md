### Trigger
> 충돌한건 아니지만 특정 영역을 지나갔다는 것을 알려줌  

탑쌓기 게임에서 **블록이 바닥에 떨어지면 실패했다**는 것을 알려줄 수 있음.  

### Trigger 동작시키기
> Collider에서 'Is Trigger'를 체크해주면 됨

### OnTriggerEnter 메소드
```c#
void OnTriggerEnter(Collider c) 
// 여기는 매개 변수가 Collider임 Collision과 혼동 x
{
 Debug.Log(c.gameObject.name); // 콘솔에 찍어보기
 if( c.gameObject.name == "Ball" )
 { 
   Application.LoadLevel("Game"); //Game은 현재 볼게임 만들고 있는 유니티 파일 이름임
                                  //Game 파일을 첨부터 다시 실행시키라는 의미.
 }
}
```
### 오브젝트 모습 안보이게 하기 
> Inspector 창에서 Mesh Renderer를 지우면 모습이 안보이게 됨  


