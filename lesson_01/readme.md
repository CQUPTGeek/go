# 1. 安装go
安装地址 go<br>
[![](https://i-blog.csdnimg.cn/blog_migrate/8f9ee00628149a12a1939b590430311d.png)]<br>



下载安装<br>

# 2. 配置go环境
[![](https://i-blog.csdnimg.cn/blog_migrate/0dfb55ff27cc3bfd3c3d89ac551735a7.png)]<br>
[![](https://i-blog.csdnimg.cn/blog_migrate/eb60878234089143abca81afa0592931.png)]<br>
[![](https://i-blog.csdnimg.cn/blog_migrate/8bce56e35d60b13cb574ed070fbcc5c6.png)]<br>
不建议安装在C盘，<br>
[![](https://i-blog.csdnimg.cn/blog_migrate/c588f95f328cde364b9ac7a8c897b315.png)]<br>
[![](https://i-blog.csdnimg.cn/blog_migrate/348a122c255afac8716bae2f43ea8c25.png)]<br>






安装成功了

# 3. 配置系统环境
我的电脑，右键  <br>

[![](https://i-blog.csdnimg.cn/blog_migrate/77cd1cca00e049aecda84ff4809548c1.png)]<br>
  然后选 高级系统设置 -> 环境变量 <br>
在环境变量这里加入GOPATH和GOROOT，并且将GO111MODULE设置成auto。<br>
GOROOT就是安装go的路径  <br>


GOPATH就是go下面的bin路径<br>
[![](https://i-blog.csdnimg.cn/blog_migrate/98fdd8945f23e2410b539ebf9799d4b4.png)]<br>
然后在系统变量上面新建配置，就是你刚刚安装go的路径，这个path！  

[![](https://i-blog.csdnimg.cn/blog_migrate/1028e07d363d6ba5a993acb85e98b2c9.png)]<br>
还是你刚刚的安装的路径。  <br>

[![](https://i-blog.csdnimg.cn/blog_migrate/a8f0ca732168353ba9fcb44967f32197.png)]<br>
重启一下电脑<br>

搜索cmd  <br>

[![](https://i-blog.csdnimg.cn/blog_migrate/d3762ef952f2954c4e7a63e4e9f40216.png)]<br>

  在cmd打开，就可以看到了<br>
[![](https://i-blog.csdnimg.cn/blog_migrate/860d510c6d059e25d667de7ccf9821d9.png)]<br>







# 4. 安装编译器
最新版：[安装地址](https://www.jetbrains.com/go/)

Goland安装<br>
[![](https://i-blog.csdnimg.cn/blog_migrate/194facb36c80ef9fb118c57b6be16ec7.png)]<br>



但是注意一下，这个是收费的，但是学生可以免费使用。<br>
具体参考：https://blog.csdn.net/qq_62390970/article/details/132346753 <br>
[![](https://i-blog.csdnimg.cn/blog_migrate/0fffeb1e03931ce7112a37b6b79c7e33.png)]<br>

[![](https://i-blog.csdnimg.cn/blog_migrate/b2edd436abcc35a944935982938457ae.png)]<br>

[![](https://i-blog.csdnimg.cn/blog_migrate/b4a6d57585f694c431b263ac9f00fc30.png)]<br>

[![](https://i-blog.csdnimg.cn/blog_migrate/3255a56cde34f48366ffc1b067d1b30e.png)]<br>
[![](https://i-blog.csdnimg.cn/blog_migrate/3b12d980f2756f4d939d4f0f7dc9f3d4.png)]<br>





# 5. 激活
打开之后编译器<br>
[![](https://i-blog.csdnimg.cn/blog_migrate/4410aba743abad5ecda3a22f6e0bb556.png)]<br>
[![](https://i-blog.csdnimg.cn/blog_migrate/14edc67b0e53543d3464b73eb1d995eb.png)]<br>



# 6. HelloWorld
运行一次HelloWorld<br>

打开Goland编译器！<br>

[![](https://i-blog.csdnimg.cn/blog_migrate/3e56498fdcea1a1f083fa60affe68431.png)]<br>

[![](https://i-blog.csdnimg.cn/blog_migrate/9721fbdfb842523e4479724c94026c6f.png)]<br>

直接create就好了
[![](https://i-blog.csdnimg.cn/blog_migrate/03b44881604175aa65ffd06da4f86c4e.png)]<br>
[![](https://i-blog.csdnimg.cn/blog_migrate/84f2eb99955009377f7f3cea7da10f8d.png)]<br>
[![](https://i-blog.csdnimg.cn/blog_migrate/8212d9f432b7cc82d58924a61c06e6a8.png)]<br>
[![](https://i-blog.csdnimg.cn/blog_migrate/87e34962bd5ad5b3a33f29fd66df37ba.png)]<br>

# Go语言基础之变量和常量

## 目录

1. 标识符与关键字
2. 变量
   - 声明
   - 初始化
   - 短变量声明
   - 匿名变量
3. 常量
   - iota
4. 注意事项

------

## 标识符与关键字123

### 标识符

- 由字母、数字和 `_` 组成，且不能以数字开头。
- 示例：`abc`, `_`, `_123`, `a123`。

### 关键字（25个）

go

复制

```
break    default     func    interface  select
case     defer       go      map        struct
chan     else        goto    package    switch
const    fallthrough if      range      type
continue for         import  return     var
```

### 保留字（37个）

包括基础类型（如 `int`, `bool`）、常量（如 `true`, `nil`）和内置函数（如 `make`, `panic`）等16。

------

## 变量

### 变量声明

#### 标准声明

go

复制

```
var 变量名 类型
var name string
var age int
```

#### 批量声明

go

复制

```
var (
    a string
    b int
    c bool
)
```

### 变量初始化12

- **默认值**：整型/浮点型为 `0`，字符串为 `""`，布尔型为 `false`，指针/切片等为 `nil`。

- **显式初始化**：

  go

  复制

  ```
  var name string = "daizhe"
  var age, isOK = 18, true
  ```

### 类型推导

编译器自动推断变量类型：

go

复制

```
var name = "daizhe"  // 类型为 string
var age = 18         // 类型为 int
```

### 短变量声明（函数内使用）

go

复制

```
func main() {
    n := 10          // 局部变量
    m := 200         // 覆盖全局变量m
    fmt.Println(m, n)
}
```

### 匿名变量

使用 `_` 忽略返回值：

go

复制

```
func foo() (int, string) { return 10, "Q1mi" }

func main() {
    x, _ := foo()    // 忽略第二个返回值
    _, y := foo()    // 忽略第一个返回值
}
```

------

## 常量

### 基本声明16

go

复制

```
const pi = 3.1415
const (
    e = 2.7182
    n1 = 100        // n1=100
    n2              // n2=100（继承上一行）
)
```

### iota计数器

- **规则**：从 `0` 开始，每新增一行常量声明递增 `1`。

- **示例**：

  go

  复制

  ```
  const (
      a1 = iota    // 0
      a2           // 1
      a3           // 2
  )
  ```

#### 常见用法

1. **跳过值**：

   go

   复制

   ```
   const (
       n1 = iota   // 0
       n2           // 1
       _            // 跳过
       n4           // 3
   )
   ```

2. **插队**：

   go

   复制

   ```
   const (
       n1 = iota   // 0
       n2 = 100     // 100
       n3 = iota    // 2
   )
   ```

3. **定义数量级**：

   go

   复制

   ```
   const (
       _  = iota
       KB = 1 << (10 * iota)  // 1 << 10 = 1024
       MB = 1 << (10 * iota)  // 1 << 20
   )
   ```

4. **多值声明**：

   go

   复制

   ```
   const (
       a, b = iota+1, iota+2  // 1, 2（iota=0）
       c, d                    // 2, 3（iota=1）
   )
   ```

------

## 注意事项

1. **变量必须使用**：未使用的变量会导致编译错误。
2. **作用域**：短变量声明 `:=` 仅限函数内部，全局变量需用 `var`。
3. **匿名变量**：`_` 不占用内存，可重复使用。


