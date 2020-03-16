# 포워딩(Forwarding) / 인클루딩(Including)

서블릿끼리 작업을 위임하는 방법 <br>

## 포워딩(Forwarding)

포워드 방식은 작업을 한 번 위임하면 다시 이전 서블릿으로 제어권이 돌아오지 않는다

- Servlet

  ```
  RequestDispatcher rd = request.getRequestDispatcher("/Error.jsp");
  rd.forward(request, response);
  ```

- JSP
  ```
  <jsp:forward page="/Error.jsp"/>
  ```

## 인클루딩(Including)

인클루드 방식은 다른 서블릿으로 작업을 위임한 후, 그 서블릿의 실행이 끝나면 다시 이전 서블릿으로 제어권이 넘어온다

- Servlet

  ```
  RequestDispatcher rd = request.getRequestDispatcher("/Header.jsp");
  rd.include(request, response);
  ```

- JSP
  ```
  <jsp:include page="/Header.jsp"/>
  ```
