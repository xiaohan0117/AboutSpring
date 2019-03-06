# 一、关于springMvc<br>
## 1、SpringMVC的工作原理：<br>
   1>用户发送请求至前端控制器（DispatcherServlet）<br>
   2>DispatcherServlet接收到请求调用处理器映射器HandlerMapping<br>
   3>处理器映射器找到具体的处理器，（可以根据xml配置，注解进行查找），生成处理器对象及处理器拦截器（有则生成）并返回给                                  DispatcherServlet<br>
   4>DispatcherServlet调用处理器适配器（HandlerAdapter）<br>
   5>处理器适配器通过适配调用具体的处理器（Controller，后台控制器）<br>
   6>Controller完成后返回ModelAndView<br>
   7>HandlerAdapter将Controller返回的ModelAndView返回给DispatcherServlet<br>
   8>DispatcherServlet将ModelAndVIew传给视图解析器（ViewReslover）<br>
   9>视图解析器解析后返回具体的View<br>
   10>DispatcherServlet根据View进行视图渲染<br>
   11>DispatcherServlet响应结果给用户<br>
                          
## 2、SpringMVC和Struts2的区别<br>
   1>**struts2**  的核心是基于Filter的，即StrutsPreparedAndExecuteFilter;<br>
    &nbsp;&nbsp;&nbsp;&nbsp;**springMVC**的核心是基于Servlet的，即前端处理器（DispatcherServlet）;<br>
   2>**struts2**  是基于类开发的，传递的参数是通过属性传递（属性驱动或者模型驱动），所以只能设计为多例模式;<br>
    &nbsp;&nbsp;&nbsp;&nbsp;**springMVC**是基于类中的方法开发的，也就是一个url对应一个方法，传递参数是传到方法的形参上面，所以既可以是单例模式的也可以是多例模式;<br>
   3>**struts2**  struts2采用的是值栈存储请求以及响应数据，OGNL存取数据;<br>
    &nbsp;&nbsp;&nbsp;&nbsp;**springMVC**采用request来解析请求内容，然后由内部的getParameter给方法中形参赋值，再把后台处理过的数据通ModelAndView对象存储，Model存储数据，VIew存储视图，再把对象通过request传递到页面去;<br>
   
