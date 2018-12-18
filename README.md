#一、关于springMvc<br>
   1、SpringMVC的工作原理：1>用户发送请求至处理器映射器（DispatcherServlet）<br>
                          2>DispatcherServlet接收到请求调用处理器映射器HandlerMapping<br>
                          3>处理器映射器找到具体的处理器，（可以根据xml配置，注解进行查找），生成处理器对象及处理器拦截器（有则生成）并返回给                                   DispatcherServlet<br>
                          4>DispatcherServlet调用处理器适配器（HandlerAdapter）<br>
                          5>处理器适配器通过适配调用具体的处理器（Controller，后台控制器）<br>
                          6>Controller完成后返回ModelAndView<br>
                          7>HandlerAdapter将Controller返回的ModelAndView返回给DispatcherServlet<br>
                          8>DispatcherServlet将ModelAndVIew传给视图解析器（ViewReslover）<br>
                          9>视图解析器解析后返回具体的View<br>
                          10>DispatcherServlet根据View进行视图渲染<br>
                          11>DispatcherServlet响应结果给用户<br>
                          
