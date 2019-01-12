### Tag?
여러개의 게임 오브젝트를 종류별로 묶어서 관리가 필요할 때 쓰는 기능  

>Inspector 창 제일 위에 Tag-> Add Tag -> + 버튼 누르고 원하는 Tag 추가

### 어디에 사용?
GameObject.FindGameObjectsWithTag("Coin");
> 이런 Tag를 가진 게임 오브젝트들의 배열을 반환.
```c#
void Start()
{
 GameObject [] coins = GameObject.FindGameObjectsWithTag("Coin");
 // Coin이란 태그 가진 게임 오브젝트들의 배열을 coins에 저장
 Debug.Log(coins[0].name);
 // 배열의 첫번째 원소 이름을 콘솔에 찍는다.
}
