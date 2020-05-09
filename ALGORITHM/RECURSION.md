# 순환(Recursion)

자기 자신을 호출하는 함수 (재귀함수)

```
    void func(...) {
        ...
        func(...);
        ...
    }
```

### 무한루프에 빠지지 않으려면?

```
    public static void func(int k) {
        if(k <= 0) // Base case
            return;
        else {
            System.out.println("Hello...");
            func(k-1); // Recursive case
        }
    }
```

- Base case : 적어도 하나의 recursion에 빠지지 않는 경우가 존재해야 한다.

- Recursive case : recursion을 반복하다보면 결국 base case로 수렴해야 한다.

### Recursion vs Interation

- 모든 순환함수는 반복문(interation)으로 변경 가능
- 그 역도 성립 즉 모든 반복문은 recursion으로 표현 가능
- 순환함수는 복잡한 알고리즘을 단순하고 알기쉽게 표현하는 것을 가능하게 함
- 하지만 함수 호출에 따른 오버해드가 있음(매개변서 전달, 액티베이션 프레임 생성 등)

### 순환적 알고리즘 설계

- 암시적(implicit) 매개변수를 명시적(explicit) 매개변수로 바꾸어라!

### 참조

- [영리한 프로그래밍을 위한 알고리즘 강좌](https://www.inflearn.com/course/%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98-%EA%B0%95%EC%A2%8C/dashboard)
