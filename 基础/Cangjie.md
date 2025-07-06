# 仓颉

`跟我一起学“仓颉”编程语言: P10`

## 基础介绍

### 安装目录
```yaml
cangjie:
    /bin:
    /lib:
    /modules:
    /runtime:
    /third_party:
    /tools:
```

语句不需要写分号`;`
环境变量：`CANGJIE_HOE`


### cjc
```yaml
cjc:
    -o: # 输出文件名
    -v:
```

仓颉编译器


### cjpm
```yaml
cjpm:
    bench:
    build: # 构建
    check:
    clean:
    init: # 初始化项目
    install:
    run: # 运行
    test:
    tree:
    uninstall:
    update:
```

仓颉包管理器


#### cjpm.toml
```yaml
cjpm.toml:
    package:
        cjc-version:
        compile-option:
        description:
        output-type:
        link-option:
        name:
        package-configuration:
        src-dir:
        target-dir:
    dependencies:
```


## 核心内容
```yaml
std:
    argopt:
    ast:
    binary:
    collection:
        concurrent:
    console:
    convert:
    core: # 语言核心包，自动引入
        print():
        println():
    crypto:
        cipher:
        digest:
    database:
        sql:
    deriving:
    env:
    fs:
    io:
    math:
    net:
    objectpool:
    overflow:
    posix:
    process:
    random:
    ref:
    reflect:
    regex:
    runtime:
    sort:
    sync: # 并发

    time:
    unicode:
    unittest: # 单元测试
```



### 数据类型
```yaml
DataType: # 9 = 3 + 2 + 2 + 2
    Bool:
    Int8:
    Int16:
    Int32:
    Int64:
    UInt64:
    Float64:
    Rune: # 字符
    String: # 字符串
    Tuple:
    Range:
    Unit: # 空类型
    Nothing:
```

#### Bool
#### Int
#### Float
#### Rune
#### String
```rust
var str: String = "xxx"

// 多行字符串
var str = """
    多行字符串
"""
```
字符串


#### Tuple
```rust
var tuple: (Int64, String) = (233, "sylvie233")
```

元组
支持命名元组

#### Range
```rust
// start..end:step 默认左闭右开
var range: Range<Int64> = 1..10:2
```

范围


#### Unit
#### Nothing




### 控制流程
```yaml
ControlFlow:
    const: # 常量定义
    func: # 函数定义
    import: # 
    let: # 变量定义，默认不可变变量
    package: # 模块定义
    var: # 可变变量定义
    do ... while:
    for in ...:
    if ... else if ... else ...: # 条件分支，支持表达式返回值
    try ... catch ... finally: # 异常处理
    while ...:
        break:
        continue:
```

运算符分类：
- 赋值运算符
- 算术运算符
- 位运算符
- 关系运算符
- 逻辑运算符


#### Exception Handler
```swift
try {
    throw NegativeArraySizeException("NegativeArraySizeException")
} catch (e: NegativeArraySizeException) {
    println("Exception info: ${e}.")
} finally {
    println("The finally block is executed.")
}
```

异常处理 `try catch finally`



### 函数
```rust
func add(a: Int64, b: Int64): Int64 {
    return a + b
}
```

函数定义：`func`
- 函数默认最后一行为返回值



### 结构体
```rust
struct Rectangle {
    let width: Int64
    let height: Int64

    public init(width: Int64, height: Int64) {
        this.width = width
        this.height = height
    }

    public func area() {
        width * height
    }
}
```


### 面向对象





### 模块






### 并发





### 宏