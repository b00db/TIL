# 테스트케이스가 주어지지 않는 경우

테스트케이스의 개수와 종료조건이 명시돼있지 않을 경우
-> 정상적인 프로그램 종료를 위해 데이터 소스로부터 더 이상 읽을 수 있는 데이터가 없음을 나타내야 하는 문제가 발생
=> 파일 끝(End of File, EOF)

### hasNext() 메서드 활용 (Int형 변수를 입력받을 땐 hasNextInt() 사용 가능)

```
Scanner scanner = new Scanner(System.in); // Scanner 클래스
while(scanner.hasNextInt()) {
    int a = scanner.nextInt();
    int b = scanner.nextInt();
    ...
}
```

- boolean hasNext() (Scanner 클래스의 주요 메서드) : 현재 입력된 토큰이 있으면 true, 아니면 입력 때까지 무한정 대기, 새로운 입력이 들어올 때 true 리턴. ctrl-z 키가 입력되면 입력 끝이므로 flase 리턴.

### 다른 언어는?

- C : <br>
  `while(scanf("%d %d", &a, &b) != EOF) {...}`
- C++ : <br>
  `while(scanf("%d %d", &a, &b) != EOF) {...}` <br>
  `while(cin >> a >> b) {...}`
