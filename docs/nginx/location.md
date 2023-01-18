### 修饰符几种情况
- / 前缀匹配
- = / 完全精确匹配
- ~* 正则表达式，不区分大小写
- ~ 正则表达式，区分大小写
- ^~ 以某个字符开头，^ 非的意思，表示不使用正则表达式

### 修饰符优先级
- =           - 完全匹配  
- ^~          - 优先匹配  
- ~ && ~*     - 正则表达式匹配  
- no modifier - 前缀匹配
- nginx 将检查是否有任何完全匹配。如果它不存在，它将寻找优先的。如果此匹配也失败，则将按出现顺序测试正则表达式匹配。如果都失败了，将使用最后一个前缀匹配