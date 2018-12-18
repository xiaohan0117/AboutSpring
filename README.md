#一、关于springMvc
   1、SpringMVC的工作原理：1>用户发送请求至处理器映射器（DispatcherServlet）
                          2>DispatcherServlet接收到请求调用处理器映射器HandlerMapping
                          3>处理器映射器找到具体的处理器，（可以根据xml配置，注解进行查找），生成处理器对象及处理器拦截器（有则生成）并返回给                                   DispatcherServlet
                          4>DispatcherServlet调用处理器适配器（HandlerAdapter）
                          5>处理器适配器通过适配调用具体的处理器（Controller，后台控制器）
                          6>Controller完成后返回ModelAndView
                          7>HandlerAdapter将Controller返回的ModelAndView返回给DispatcherServlet
                          8>DispatcherServlet将ModelAndVIew传给视图解析器（ViewReslover）
                          9>视图解析器解析后返回具体的View
                          10>DispatcherServlet根据View进行视图渲染
                          11>DispatcherServlet响应结果给用户
                          
