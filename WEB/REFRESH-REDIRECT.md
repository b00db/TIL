# 리프래시(Refresh) / 리다이렉트(Redirect)

하나의 화면에서 다른 화면으로 자동으로 이동하게 할 때 사용하는 기술 <br>

## 리프래시(Refresh)

일정 시간이 지나고 나서 자동으로 서버에 요청을 보내는 방법 <br>
우리 말로 '새로 고침'이라고 한다.

### 구현 방법

- 응답 헤더를 이용한 리프래시

  - `reponse.addHeader("Refresh", "1;url=list");`
  - `reponse.setHeader("Refresh", "1;url=list");`

- HTML의 meta 태그를 이용한 리프래시
  - `<meta http-equiv='Refresh' content='1; url=list'>` <br>

## 리다이렉트(Redirect)

정보를 등록하고 나서 결과를 출력하지 않고 즉시 다른 화면으로 이동하게 하는 방법

### 구현 방법

- 리다이렉트 메서드 sendRedirect()
  - `response.sendRedirect("list");`
