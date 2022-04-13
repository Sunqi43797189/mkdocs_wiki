### 函数参数
- 实际参数：函数实际调用时传入的参数
- 形式参数：把参数列表中的参数
![](/images/golang/function.jpg)

### 传参
- 函数参数传递采用是值传递的方式
- 所谓“值传递”，就是将实际参数在内存中的表示逐位拷贝（Bitwise Copy）到形式参数中
- 对于像整型、数组、结构体这类类型，它们的内存表示就是它们自身的数据内容，因此当这些类型作为实参类型时，值传递拷贝的就是它们自身，传递的开销也与它们自身的大小成正比
- 像 string、切片、map 这些类型它们的内存表示对应的是它们数据内容的“描述符”。当这些类型作为实参类型时，值传递拷贝的也是它们数据内容的“描述符”，不包括数据内容本身，所以这些类型传递的开销是固定的，与数据内容大小无关

### 函数传参例外
- 对于类型为接口类型的形参，Go 编译器会把传递的实参赋值给对应的接口类型形参
- 对于为变长参数的形参，Go 编译器会将零个或多个实参按一定形式转换为对应的变长形参
- 变长参数实际上是通过切片来实现

### Go函数特征
- 多个可以命名的返回值
- 函数可以存储在变量中
- 支持在函数内创建并通过返回值返回
- 可以作为参数传入函数
- 拥有自己的类型`type HandlerFunc func(ResponseWriter, *Request)`

### 函数健壮性原则
- 不要相信任何外部输入的参数
- 不要忽略任何一个错误
- 不要假定异常不会发生