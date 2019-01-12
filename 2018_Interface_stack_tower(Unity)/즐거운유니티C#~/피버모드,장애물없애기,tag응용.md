강의자는 redcoin을 만들었음.

```c#
//redcoin 먹었을 때의 메소드에서
//DestroyObstacles() 메소드를 호출함

void DestroyObstacles()
{
  GameObject[] obstacles = GameObject.FindGameObjectsWithTag("Obstacle");
  for(int i= 0 ; i<obstacles.Length ; i++)
  {
    Destroy(obstacles[i]);
  }
}
```
