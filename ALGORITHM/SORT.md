# 정렬(Sort)

```
- 버블 정렬(Bubble sort)
- 삽입 정렬(Insertion sort)
- 선택 정렬(Selection sort)

> simple, slow
```

```
- Quicksort
- Merge sort
- Heap sort

> fast
```

```
- Radix sort

> O(N)
```

<br>

## 선택 정렬(Selection Sort)

![Selection Sort](/ALGORITHM/img/selection_sort.PNG)

```
selectionSort(A[], n)  // 배열 A[1...n]을 정렬
{
    for last <- n downto 2 {  // ⅰ
        A[1...last] 중 가장 큰 수 A[k]를 찾는다;  // ⅱ
        A[k] <-> A[last];  // A[k]와 A[last]의 값을 교환  ⅲ
    }
}
```

- 실행시간: <br>
  ⅰ의 for 루프는 n-1번 반복 <br>
  ⅱ에서 가장 큰 수를 찾기 위한 비교횟수: n-1, n-2, ..., 2, 1 <br>
  ⅲ의 교환은 상수시간 작업 <br>
- 시간복잡도 T(n) = (n-1)+(n-2)+...+2+1 = n(n-1)/2 = O(n^2)

<br>

## 버블 정렬(Bubble Sort)

![Bubble Sort](/ALGORITHM/img/bubble_sort.PNG)

```
bubbleSort(A[], n)  // 배열 A[1...n]을 정렬
{
    for last <- n downto 2 {  // ⅰ
        for i <- 1 to last-1  // ⅱ
            if(A[i]>A[i+1]) then A[i] <-> A[i+1];  // 교환  ⅲ
    }
}
```

- 실행시간: <br>
  ⅰ의 for 루프는 n-1번 반복 <br>
  ⅱ의 for 루프는 각각 n-1, n-2, ..., 2, 1 번 반복 <br>
  ⅲ의 교환은 상수시간 작업 <br>
- 시간복잡도 T(n) = (n-1)+(n-2)+...+2+1 = n(n-1)/2 = O(n^2)

<br>

## 삽입 정렬(Insertion Sort)

![Insertion Sort](/ALGORITHM/img/insertion_sort.PNG)

![Insertion](/ALGORITHM/img/insertion.PNG)

```
insertionSort(A[], n)  // 배열 A[1...n]을 정렬
{
    for(i <- 2 to n) {  // ⅰ
        A[1...i]의 적당한 자리에 A[i]를 삽입한다;  // ⅱ
    }
}
```

- 실행시간: <br>
  ⅰ의 for 루프는 n-1번 반복 <br>
  ⅱ의 삽입은 최악의 경우 i-1번 비교 <br>
- 최악의 경우 시간복잡도 T(n) = (n-1)+(n-2)+...+2+1 = n(n-1)/2 = O(n^2)

<br>

### 참조

- [영리한 프로그래밍을 위한 알고리즘 강좌](https://www.inflearn.com/course/%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98-%EA%B0%95%EC%A2%8C/dashboard)
