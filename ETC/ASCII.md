# 아스키 코드 값 출력하기

개념: 문자로 입력 받고, 숫자로 변환하여 출력한다.

### C

```
#include <stdio.h>

int main()
{
    char c;
    scanf("%c", &c);
    printf("%d", c);
}
```

### C++

```
#include <iostream>

int main()
{
    char c;
    std::cin>>c;
    std::cout<<(int)c;
}
```

### Java

```
import java.util.Scanner;
​
public class Main {
​
    public static void main(String[] args) {

        Scanner scanner = new Scanner(System.in);

        String input = scanner.next();
        char c = input. charAt(0);

        // char 값을 int로 변환하여 출력 (아스키코드 값)
        System.out.println((int)c);

    }
​
}
```

```
import java.io.IOException;

public class Main {
    public static void main(String[] args) throws IOException{
        int c = System.in.read();
        System.out.println(c);
    }
}
```

```
import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;

public class Main {
    public static void main(String[] args) throws IOException{
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        int c =  br.read();
        System.out.println(c);
    }
}
```
