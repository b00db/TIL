# Java 소수점 자릿수 지정 표현하기

### 1. Math 클래스 이용

- Math.round() // 반올림
- Math.ceil() // 올림
- Math.floor() // 내림

```
double num = 80.153;
System.out.println(num);

System.out.println("반올림(소수점 첫째자리에서 반올림): " + Math.round(num));               // 소수점 첫째자리에서 반올림
System.out.println("반올림(소수점 첫번째자리까지 표시): " + Math.round((num) * 10) / 10.0);      // 소수점 첫번째자리까지 표시
System.out.println("반올림(소수점 두번째자리까지 표시): " + Math.round((num) * 100) / 100.0);    // 소수점 두번째자리까지 표시

System.out.println("올림: " + Math.ceil(num));    // 올림
System.out.println("버림: " + Math.floor(num));    //버림
```

```
80.153
반올림(소수점 첫째자리에서 반올림): 80
반올림(소수점 첫번째자리까지 표시): 80.2
반올림(소수점 두번째자리까지 표시): 80.15
올림: 81.0
버림: 80.0
```

`Math.round(숫자)에 10^n 만큼 곱한 후 다시 10^n 으로 나누면, 소수점 n째자리까지 나타낼 수 있다.`

### 2. System.out.printf() 이용

```
double num = 80.1532;
System.out.println(num);

System.out.printf("소수점 두번째자리까지 표시: %.2f\n", num); // 소수점 두번째자리까지 표시
System.out.printf("소수점 네번째자리까지 표시: %.4f\n", num); // 소수점 네번째자리까지 표시
```

```
80.1532
소수점 두번째자리까지 표시: 80.15
소수점 네번째자리까지 표시: 80.1532
```

`%: 데이터, .n: n자리(소수점 아래 자리수 지정. 잘리는 소수점 자리수는 반올림 시켜서 표시.), f: 실수`
