## c++에서 pair로된 값 lower_bound 사용하기

우리가 흔히 `lower_bound`를 사용할 때는 다음과 같다.
👉 lower_bound(x): x이상인 값 중 가장 작은 값

만약 x가 pair로 된 값이면서 x.first가 target 이상인 값을 찾으려면 어떻게 해야할까?

이럴 땐 `lower_bound({target, -INF})`로 찾아주면 된다.
