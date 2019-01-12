> Ball 프로젝트 참고  

1.Transform Position
---
**transform.position.x** |-> x좌표의 위치

```c#
public class Ball : MonoBehaviour {
float startingPoint;

void Start() {
startingPoint = transform.position.z; //게임 시작시 처음 z좌표 저장
}

void Update() {
distance= transform.position.z - startingPoint; //distance 계산, 
                                                //매 프레임마다 distance 늘어남
}
}
```
