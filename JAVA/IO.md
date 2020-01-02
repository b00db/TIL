# BufferedReader와 BufferedWriter를 활용한 빠른 입출력하기

Scanner와 System.out.println 대신 BufferedReader와 BufferedWriter를 사용할 수 있다.

### 왜?

- 주로 코딩테스트에서 입출력 방식이 느리면 여러 줄을 입력 받거나 출력할 때 시간초과가 날 수 있다.
- 특히 반복문 주의!

### BufferedReader 사용법

```BufferedReader br = new BufferedReader(new InputStreamReader(System.in)); // 선언
    String s = br.readLine(); // String
    int i = Integer.parseInt(br.readLine()); // int
```

공백단위 구분 ⅰ. StringTokenizer 클래스의 nextToken() 메소드 사용

```StringTokenizer st = new StringTokenizer(s, " ");
    int a = Integer.parseInt(st.nextToken()); // 첫 번째 호출
    int b = Integer.parseInt(st.nextToken()); // 두 번째 호출
```

공백단위 구분 ⅱ. String 클래스의 split() 메소드 사용

```
String array[] = s.split(" "); // 공백마다 데이터를 끊어서 배열에 넣음
```

※ readLine 할 때마다 예외처리! -> 대게 'throws IOException', 'throws Exception' 사용

### BufferedWriter 사용법

```BufferedWriter bw = new BufferedWriter(new OutputStreamWriter(System.out)); // 선언
    String s = "abcdefg"; // 출력할 문자열
    bw.write(s + "\n"); // 출력
    bw.flush(); // 남아있는 데이터를 모두 출력시킴
    bw.close(); // 스트림을 닫음
```

### 정리

- BufferedReader: 문자 버퍼 입력, 라인 해석
- InputStreamReader: 바이트 스트림을 문자 스트림으로 변환
- BufferedWriter: 문자 스트림에 버퍼 출력, 줄바꿈 사용
- OutputStreamWriter: 문자 스트림을 바이트 파일로 변환

### 다른 언어는?

- C++ : cin / cout 을 사용하고자 한다면, cin.tie(NULL) 과 syn_with_stdio(false) 를 둘 다 적용해주고, endl 대신 개행문자(\n)를 쓰자. 단, 이렇게 하면 더 이상 scanf/printf/puts/getchar/putchar 등 C의 입출력 방식을 사용하면 안 된다.
- Python : input 대신 sys.stdin.readline을 사용할 수 있다. 단, 이때는 맨 끝의 개행문자까지 같이 입력받기 때문에 문자열을 저장하고 싶은 경우 .rstrip()을 추가로 해주는 것이 좋다.
- C : scanf / printf 는 충분히 빠르다.
