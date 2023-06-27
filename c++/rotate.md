## rotate

`#include <algorithm>` 내장 함수

단순 구현문제에서 **회전**을 이용해야 하는, 아주 귀찮은 문제들을 풀 때 유용함

rotate(시작 iterator, 첫 위치로 올 forward iterator, 종료 iterator)

ex)

```cpp
rotate(v.begin(), v.begin() + 1, v.end()); // 왼쪽으로 1칸씩 이동
rotate(v.begin(), v.begin() + 2, v.end()); // 왼쪽으로 2칸씩 이동

rotate(v.begin(), v.begin() - 1, v.end()); // 오른쪽으로 1칸씩 이동
rotate(v.begin(), v.begin() - 3, v.end()); // 오른쪽으로 3칸씩 이동
```
