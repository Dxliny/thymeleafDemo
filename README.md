# demo for thymeleaf
1.先将thymeleaf导入
   <dependency>
      <groupId>javax</groupId>
      <artifactId>javaee-web-api</artifactId>
      <version>7.0</version>
      <scope>provided</scope>
    </dependency>
    <!-- Compile dependencies -->
    <dependency>
      <groupId>org.thymeleaf</groupId>
      <artifactId>thymeleaf</artifactId>
      <version>3.0.7.RELEASE</version>
    </dependency>
2.在html界面引入thymeleaf
  <html  xmlns:th="http://java.sun.com/jsf/core">
3.th:text"${user.name}"
  将后台数据中的user对象获取，并直接展示
4.th:inclued="@{login.html}"
  将login.html页面引入本页面，例子@{/page/success.html}
5.th:each="user:${userList}"
  将用户列表获取到并利用user将其遍历,例子
  <!--<ul>
    <li th:each="user:${userList}">
      <span th:text="${user.name}"></span>
    </li>
  </ul>-->
6. th:each="map:${myMap}"
  将map键值对获取到并利用map将其遍历,例子
   <!--<ul>
    <li th:each="map:${myMap}">
      <span th:text="${map.key}"></span>
      <!-- map(String,User) -->
      <span th:text="${map.value.name}"></span>
    </li>
  </ul>-->
