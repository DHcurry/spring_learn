# spring mvc 学习笔记
## 简单demo的执行过程
### 配置web.xml
web.xml要做的就是配置好servlet,并配置启动时就加载springmvc.xml的配置文件,配置的目的就是利用spring的ioc容器创建一些工具

### 配置springmvc.xml
springmvc.xml文件本身就是一个spring bean的配置文件,我们在deom中有一个视图解析器,在该项目中的视图解析器就是接收controller返回的string,该视图解析器会根据名称和位置匹配相应的jsp文件

## 请求参数的绑定
### 请求参数与方法属性对应
这个我们可以参考param.jsp的第一个方法
### 请求参数封装到类中
我们要保证input中的name与类中属性名字相对应
### 请求参数封装到复合类中(类中含类)
可以继续参考param中的代码
### 请求参数封装到有列表的类中

## 请求参数数据类型转换
请求参数一般都是用string的方式传递，很多工具类可以将string转换成常见的类型，如integer等，但还有很多类型是没法转换，因此要自定义一些转换类将string转换成其他类型