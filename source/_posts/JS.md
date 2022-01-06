---
title: JS
date: 2021-07-03 15:46:06
tags:
  - 前端
  - js
categories:
  - 前端
cover: https://w.wallhaven.cc/full/vm/wallhaven-vmjye3.jpg
---

## JS

### 编程语言

#### 编程

- **编程：**就是让计算机为解决某个问题而使用某种程序设计语言编写程序代码，并最终得到结果的过程
- **计算机程序**：就是计算机所执行的一系列的**指令集合**，而程序全部都是用我们所掌握的语言来编写的，所以人们要控制计算机一定要通过计算机语言向计算机发出命令

#### 计算机语言

- 计算机语言指用于人与计算机之间通讯的语言，他是人与计算机之间传递信息的媒介
- 分类：
  1. **机器语言**：计算机最终所执行的都是机器语言，他是由0和1组成的二进制数，二进制是计算机语言的基础
  2. **汇编语言**：和机器语言实质是相同的，都是直接对硬件操作，只不过指令采用了英文缩写的 标识符，容易识别和记忆
  3. **高级语言**：主要是相对于低级语言而言，它并不是特指某一种具体的语言，而是包括了很多编程语言

#### 编程语言

- 定义：可以通过类似于人类语言的“语言”来控制计算机，让计算机为我们做事，这样的语言就叫做编程语言
- 编程语言是用来控制计算机的一系列指令，他有固定的格式和词汇，必须遵守 
- 如今的编程语言有两种形式：汇编语言和高级语言

#### 编程语言和标记语言的区别

- 编程语言有很强的逻辑和行为能力。在编程语言里，你会看到i很多的  if else 、for、while等具有逻辑性和行为能力的指令，这是主动的
- 标记语言（html)不同于向计算机发出指令，常用于格式化和链接。标记语言的存在是用来被读取的，他是被动的

### 计算机基础

### 初识Javascript

- js是运行在客户端的脚本语言
- 脚本语言：不需要编译，运行过程中由js解释器（js引擎）逐行来进行解释并执行
- 现在也可以基于Node.js技术进行服务器端编程
- 作用：
  1. 表单动态效验（密码强度检测）（js产生最初的目的）
  2. 网页特效
  3. 服务端开发（Node.js）
  4. 桌面程序（Electron）
  5. APP（Cordova）
  6. 控制硬件-物联网（Ruff）
  7. 游戏开发（cocos2d-js)

- 浏览器执行js简介
  - 浏览器分为两部分
    1. 渲染引擎：用来解析HTML与CSS，俗称内核，比如chrome浏览器的blink，老版本的webkit
    2. js引擎：也称为JS解释器。用来读取网页中的Javascript代码，对齐处理后运行，比如chrome浏览器的v8
  - 浏览器本身不会执行js代码，而是通过内置Javascript引擎来执行JS代码。JS引擎执行代码时逐行解释每一句源码（转换为机器语言），然后由计算机去执行，所以Javascript语言归为脚本语言，会逐行解释执行。

- JS的组成
  - Javascript语法       ECMAScript
  - 页面文档对象模型   DOM
  - 浏览器对象模型       BOM

- Js的书写位置
  - 行内式
  - 内嵌式
    - 外部JS，新建.js文件	

### Js输入输出语句

| 方法             | 说明                           | 归属   |
| ---------------- | ------------------------------ | ------ |
| alert(msg)       | 浏览器弹出警示框               | 浏览器 |
| console.log(msg) | 浏览器控制台打印输出信息       | 浏览器 |
| prompt(info)     | 浏览框弹出输入框，用户可以输入 | 浏览器 |

### 变量

**类似于其他编程语言**

#### 使用

- ```javascript
  var age;//声明一个名称为age的变量
  ```

- var是一个JS关键字，用来声明变量。使用该关键字声明变量后，计算机会自动为变量分配内存空间，不需要程序员管

#### 声明的特殊情况

| 情况                       | 说明                   | 结果                |
| -------------------------- | ---------------------- | ------------------- |
| var age ;console.log(age); | 只声明 不赋值          | undefined(未定义的) |
| console.log(age)           | 不声明 不赋值 直接使用 | 报错                |
| age =10;console.log(age);  | 不声明 只赋值          | 10                  |

#### 变量命名规范

![变量命名规范](D:\前端\笔记\前端照片\变量命名规范.png)

### 数据类型

#### 变量的数据类型

- Javascript是一种弱类型的语言或者说动态语言。这意味着不用以前声明变量的类型，在程序运行过程中，类型会被自动确定
- js的变量数据类型是只有程序在运行过程中，根据等号右边的值来确定的
- js拥有动态类型，同时也意味着相同的变量可用作不同的类型

#### 分类

##### 简单型

- | 简单数据类型 | 说明                                               | 默认值    |
  | ------------ | -------------------------------------------------- | --------- |
  | Number       | 数字型，包含整数型和浮点型值，如 21、0.21          | 0         |
  | Boolean      | 布尔值类型，如true、false，等价于1和0              | false     |
  | String       | 字符串类型，如张三，注意咱们js里面，字符串都带引号 | “   ”     |
  | Undefined    | var a; 声明了变量a但没有给值，此时a=undefined      | undefined |
  | Null         | var a =null ;声明了变量a为空值                     | null      |

- ###### 数字型

  1. 前面加0是八进制，加ox是十六进制 

  2. 范围：

     ```javascript
     alert(Number.MAX_VALUE);//1.7976931348623157e+308
     alert(Number.MIN_VALUE);//5e-324
     ```

  3. 三个特殊值

     ```javascript
     alert(Infinity);//代表无穷大，大于任何数值
     alert(Infinity);//代表无穷小，小于任何数值
     alert(NaN);//代表一个分数值
     ```

  4. isNaN()这个方法用来判断一个变量是否为非数字的类型，返回true或者false

     - x是数字，返回false
     - x不是数字，返回true

- ###### 字符串型

  1. 单双都可以用，但Js这里推荐用单引号

  2. js可以做到单引号嵌套双引号，或者双引号嵌套单引号（外单内双，外双内单）

  3. 字符串转义型

     | 转义符 | 解释说明                 |
     | ------ | ------------------------ |
     | \n     | 换行符，n是newline的意思 |
     | \\\    | 斜杠\                    |
     | \\'    | ‘单引号                  |
     | \\"    | ”双引号                  |
     | \t     | tab缩进                  |
     | \b     | 空格，b是blank的意思     |

  4. 字符串长度

     - 字符串是由若干字符组成的，这些字符的数量就是字符串的长度。通过字符串的length属性可以获取整个字符串的长度 

  5. 字符串的拼接

     - 多个字符串之间可以使用+号进行拼接，其拼接方式为**字符串+任何类型=拼接之后的新字符串**
     - 拼接前会把与字符串相加的任何类型转换为字符串，在拼接成一个新的字符串

#### 获取数据类型

- typeof可用来获取检测变量的数据类型

- ```javascript
  console.log(typeof flag);
  ```

- **prompt取过来的值是字符型的**

#### 数据类型转换

##### 转换为字符串

- | 方式               | 说明                         | 案例                                 |
  | ------------------ | ---------------------------- | ------------------------------------ |
  | toString()         | 转成字符串                   | var num =1; alert(num.toString());   |
  | String()强制转换   | 转成字符串                   | var num =1; alert(String());         |
  | **加号拼接字符串** | 和字符串拼接的结果都是字符串 | var num =1; alert(num+"我是字符串"); |

##### 转换为数字型

| 方式                   | 说明                                                  | 案例                |
| ---------------------- | ----------------------------------------------------- | ------------------- |
| parselnt(string)函数   | 将string类型转成整数数值型,取整（直接舍弃后面的小数） | parselnt('78')      |
| parseFloat(string)函数 | 将string类型转成浮点数数值型                          | parseFloat('78.21') |
| Number()强制转换函数   | 将string类型转成数值型                                | Number('12')        |
| js隐式转换(-*/)        | 利用算术运算隐式转换为数值型                          | '12'-0              |

##### 转换为布尔型

- | 方式          | 说明                 | 案例             |
  | ------------- | -------------------- | ---------------- |
  | Boolean()函数 | 其他类型转换为布尔值 | Boolean('true'); |

- 代表空、否定的值会被转换为false，如‘ ’、0、NaN、null、undefined

- 其余值会被转换为true

### 运算符

#### 算数运算符

- 类似于C和C++
- 浮点数值的最高精度是17位小数，但在进行算数计算时其精度远远不如整数
- 不要直接判断两个浮点数是否相等

#### 比较运算符

- 大部分和C类似

- | 运算符名称  | 说明                        | 案例      | 结果  |
  | ----------- | --------------------------- | --------- | ----- |
  | ==          | 判等号（会转型）            | 37==37    | true  |
  | ===     !== | 全等 要求值和数据类型都一致 | 37==='37' | false |

#### 逻辑运算符

- 类似于C
- 短路运算（逻辑中断）
  1. 逻辑与
     - 语法：表达式1&&表达式2
     - 如果第一个表达式的值为真，则返回表达式2
     - 如果第一个表达式的值玩为假，则返回表达式1
  2. 逻辑或
     - 语法：表达式1&&表达式2
     - 如果第一个表达式的值为真，则返回表达式1
     - 如果第一个表达式的值玩为假，则返回表达式2

#### 运算符优先级

![运算符优先级](D:\前端\笔记\前端照片\运算符优先级.png) 

### 数组

#### 创建数组的方式

- 利用new创建数组

  ```javascript
  var 数组名 =new Array();
  var arr=new Array();//创建一个新的空数组
  ```

- 利用数组字面量创建数组

  ```javascript
  //1.使用数组字面量方式创建空的数组
  var 数组名 = [];
  //2.使用数组字面量方式创建带初始值的数组
  var 数组名 = ['小白','小黑','大黄','瑞奇'];
  ```

- 里面可以放任意类型的变量

#### 数组的长度

- 使用“数组名.length”可以访问数组元素的数量（数组长度）
- 动态监测数组元素的个数
- 想要输出多个变量，用逗号分隔开即可

#### 数组中新增元素

- 通过修改length长度来实现数组扩容的目的

- length属性时可读写的

- 新增数组元素，修改索引号，追加数组元素

- ```javascript
  var arr['red','green','blue'];
  arr[3]='pink';
  console.log(arr);
  arr[4]='hotpinl';
  console.log(arr);
  ```

- 不要直接给数组名赋值，否则会提换原来的数组内容

### 函数

- ```javascript
  function 函数名 () {
  	函数;
  }
  ```

- 如果实参的个数和形参个数一致，则输出正常结果

- 如果实参的个数多于形参的个数 ，会取的形参的个数

- 如果实参的个数小于形参的个数，多于的形参定义为undefined 最终的结果就是NaN

#### 返回值

- return语句之后的代码不被执行
- return只能返回一个值，如果用多个逗号隔开多个值，以最后一个为准

#### arguments的使用

- 当我们不确定有多少个参数传递时，可以使用arguments来获取，在JavaScript中，arguments实际上他还当前函数的一个内置对象，所以函数都内置了一个arguments对象，arguments对象中存储了传递的所有实参
- arguments展示形式是一个伪数组，因此可以进行遍历，伪数组具有以下特点：
  - 具有length属性
  - 按索引的方式储存数据
  - 不具备数组的push，pop等方法

#### 第二种函数表达方式

- var fun = function(aru) {

  ​		函数内容；

  }

  //调用

  fun();

- fun是变量名，不是函数名

- 函数表达式声明方式跟声明变量差不多，只不过变量里面存的是值而函数表达式里面存的是函数

- 函数表达式也可以进行传递参数

### 作用域

#### 作用域(es5)

- 全局作用域
  1. 整个script标签里，和.js文件里

- 局部作用域
  1. 在函数内部就是局部作用域
  2. 又叫**函数作用域**

#### 变量作用域

- 全局变量
  1. 在全局作用域下的变量
  2. **在函数内部没有声明直接赋值的变量也属于全局变量**
  3. 只有在关闭浏览器的时候才会销毁，比较占内存

- 局部变量
  1. 在函数内部声明的变量，只能在函数内部使用
  2. 函数形参也属于局部变量
  3. 当我们程序执行完毕就会销毁，比较节约内存资源

#### 块级作用域

- 目前js没有块级作用域
- js在es6的时候新增的块级作用域

#### 作用域链

- 内部函数访问外部函数的变量，采用的是链式查找的方式来决定取那个值，这种结构我们称之为作用域链
- 就近原则

### 预解析

#### 预解析

- js引擎运行分为两步：
  1. **预解析**：js引擎会把js里面所有的var还有function提升到当前作用域的最前面
  2. **代码执行**：按照代码书写顺序从上往下执行

- 预解析分为
  1. **变量预解析（变量提升）**：把所有的变量声明提升到当前作用域的最前面   不提升赋值操作
  2. **函数预解析（函数提升）**：把所有的函数声明提升到当前作用域的最前面    不调用函数

### 对象

#### 组成

- 属性：事物的特征，在对象中用属性来表示
- 方法：事物的行为，在对象中用方法来表示

#### 创建方式

- 利用字面量创建数组

  1. ```javascript
     var obj {
         uname: '张三丰'，
         age:18,
         sex:'男'，
         sayHi: function () {
             console.log(Hi~);
         }
     }
     ```

  2. 里面属性或者方法我们采取键值对的形式 键 属性 ：值  属性值

  3. 多个属性或者方法中间用逗号隔开的

  4. 方法冒号后面跟的是一个匿名函数

  5. 使用对象的两种方式：

     ```javascript
     1.console.log(obj.uname);
     2.console.log(obj['age']);
     3.obj.sayHi();
     ```

- 利用new Object创建对象

  1. ```javascript
     var obj= new Object();//创建了一个空的对象
     obj.uname='张三丰'；
     obj.age=18;
     obj.sex='男';
     obj.sayHi=function() {
         console.log('Hi~');
     }
     ```

- 利用构造函数创建对象

  1. 就是把 我们对象里面的一些相同属性和方法抽象出来封装到函数里面

  2. ```javascript
     function Star (uname,age,sex){
         this.name=uname;
         this.age=age;
         this.sex=sex;
     }
     var ldh =new Star('刘德华',18,'男');//
     ```

  3. 构造函数名字首字母要大写

  4. 我们构造函数不需要return就可以返回结果

  5. new的一个作用就是返回对象

#### 遍历对象

- for...in语句用于对数组或者对象的属性进行循环操作

- ```javascript
  for(var k in obj){
      console.log(k);//k 变量 输出 得到的是属性名
      console.log(obj[k]);//obj[k]得到的是属性值
  }
  ```

#### 内置对象

JS语言自带的一些对象，这些对象供开发者使用，并提供了一些常用的或者最基本而必要的功能（属性和方法）

##### 查文档

- 通过MDN/W3C来查询

##### math内置对象

![Math内置对象](D:\前端\笔记\前端照片\Math内置对象.png)

- Math.random()

  返回一个随机小数

- 返回两个数之间的随机整数并且包含这两个整数	

- ```javascript
  function geRandom(min,max)
  {
      return Math.floor(Math.random()*(max-min+1))+min;
  }
  ```

##### Date内置对象

- ```javascript
  //Date()日期对象 是一个构造函数必须使用new来调用创建我们的日期对象
  var arr = new Array();//创建一个数组对象
  var obj = new Object();//创建一个对象实例
  //1.使用Date如果没有参数 返回当前系统的当前时间
  var date = new Date();
  console.log(date);
  //2.参数常用的写法 数字型 2019，10，01或者是字符串型'2019-10-1 8:8:8'
  var date1 = new Date(2019,10,1);
  comsole.log(date1);//返回对不是11月是10月
  var date2 = new Date('2019-10-1 8:8:8');
  console.log(date2);
  ```

- 

![日期格式化](D:\前端\笔记\前端照片\日期格式化.png)

- 写星期的最好方法就是写一个数组，然后调用

- ```javascript
  var=['星期日','星期一','星期二','星期三','星期四','星期五','星期六']；
  var day=date。getDay();
  console.log('今天是:'+arr[day]);
  ```

- 获取日期的总的毫秒数(时间戳)

  - Date对象是基于1970年1月1日（世界标准时间）起的毫秒数

  - 通过valueOf()  getTime()获取

  - 直接写date 

    ```javascript
    var date1=+new Date();
    console.log(date1);
    ```

  - H5新增方法

    ```javascript
    console.log(Date.now());
    ```


##### 数组对象Array

- 创建方式

  1. 字面量方式   var arr =[1,2,3];

  2. new Array()   

     ```javascript
     var arr1 = new Array();//创建一个空数组
     var arr1 = new Array(2);//创建一个有两个空元素的数组，2时数组长度
     var arr1 = new Array(2，3);//等价于[2，3]
     ```

- 检测是否为数组

  - instanceof 运算符  它可以用来检测是否为数组

    ```javascript
    var arr=[];
    console.log(arr instanceof Array);
    ```

  - Array.isArray()        //H5新增的方法  ie9以上版本才支持

    ```javascript
    var arr=[];
    Array.isArray(arr);//true
    ```

- 添加删除数组元素的方法

  | 方法名               | 说明                                                       | 返回值               |
  | -------------------- | ---------------------------------------------------------- | -------------------- |
  | push(参数1,...)      | 末尾添加一个或者多个元素，注意修改原数组                   | 并返回新的长度       |
  | pop()                | 删除数组最后一个元素，把数组元素长度减一无参数，修改原数组 | 返回它删除元素的值   |
  | unshift(参数1，....) | 向数组的开头添加一个或者更多元素，注意修改原数组           | 并返回新的长度       |
  | shift()              | 删除数组的第一个元素，数组元素减1无参数，修改原数组        | 并返回第一个元素的值 |

- 数组排序

  | 方法名    | 说明                         | 是否修改原数组                    |
  | --------- | ---------------------------- | --------------------------------- |
  | reverse() | 颠倒数组中元素的顺序，无参数 | 该方法会改变原理的数组 返回新数组 |
  | sort()    | 对数组的元素进行排序         | 该方法会改变原来的数组 返回新数组 |

  ```javascript
  var arr1 = [13,4,77,1,7];
  arr1.sort(function(a,b){
      return a-b;//按照升序排列
      return b-a;//按照降序排列
  })
  console.log(arr1);
  ```

- 数组索引方法

  | 方法名                           | 说明                           | 返回值                                   |
  | -------------------------------- | ------------------------------ | ---------------------------------------- |
  | indexOf("寻找的元素",开始的位置) | 数组中查找给定元素的第一个索引 | 如果存在返回索引号，如果不存在，则返回-1 |
  | IastindexOf()                    | 在数组中的最后一个索引         | 如果存在返回索引号，如果不存在，则返回-1 |

- 数组转化为字符串

  | 方法名         | 说明                                       | 返回值         |
  | -------------- | ------------------------------------------ | -------------- |
  | toString()     | 把数组转换为字符串，逗号分隔每一项         | 返回一个字符串 |
  | join('分隔符') | 方法用于把数组中的所有元素转化为一个字符串 | 返回一个字符串 |

- | 方法名   | 说明                                    | 返回值                                         |
  | -------- | --------------------------------------- | ---------------------------------------------- |
  | concat() | 连接两个或多个数组 不影响原数组         | 返回一个新的项目                               |
  | slice()  | 数组截胡slice(begin,end)                | 返回被截胡项目的新数组                         |
  | splice() | 数组删除splic(第几个开始，要删除的个数) | 返回被删除项目的新数组，注意，这个会影响原数组 |


##### 字符串对象

- 基本包装类型

  - 为了方便操作基本数据类型，js还提供了三个特殊引用类型：String、Number、Boolean

  - 基本包装类型就是把简单数据类型包装为复杂数据类型，这样基本数据类型就有了属性和方法

  - ```javascript
    //下面代码有什么问题？
    var str = 'andy';
    console.log(str.length);
    ```

    基本数据类型是没有属性和方法，而对象才有属性和方法，但上面代码却可以执行，这是因为js会把基本数据类型包裹为复杂数据类型，其执行过程如下：

  - ```javascript
    //1.生成临时变量，把简单类型包装为复杂数据类型
    var temp = new String('andy');
    //2.赋值给我们声明的字符变量
    str = temp;
    //3.销毁临时变量
    temp = null;
    ```

- 字符串的不可变

- 不要大量拼接字符串

- 根据字符返回位置

  - 字符串所有的方法，都不会修改字符串本身（字符串是不可变的），操作完成会返回一个新的字符串

  - | 方法名                                 | 说明                                                         |
    | -------------------------------------- | ------------------------------------------------------------ |
    | indexOf('要查找的字符','开始的位置')； | 返回指定内容在元字符串中的位置，如果找不到就返回-1，开始的位置是index索引号 |
    | lastIndexOf()                          | 从后i往前找，只找第一个匹配的                                |


- 根据位置返回串

  - | 方法名            | 说明                                     | 使用                         |
    | ----------------- | ---------------------------------------- | ---------------------------- |
    | charAt(index)     | 获取指定位置的字符(index  字符的索引号)  | str.charAt(0)                |
    | charCodeAt(index) | 获取指定位置字符的ASCll码（index索引号） | str,charCodeAt()             |
    | str[index]        | 获取指定位置的字符                       | HTML5,IE8+支持和charAt()等效 |

- 字符串操作方法

  ![字符串操作方法](D:\前端\笔记\前端照片\字符串操作方法.png)

#### 面向对象

##### 构造函数

- ```javascript
      function Person(name, age) {
          this.name = name;
          this.age = age;
          this.sayHello = function() {
              alert(this.name);
          }
      }
    		Person('vcedqwa',14);//构造函数
  ```

##### 继承

- 通过普通函数调用this指向window

- 通过对象的成员函数调用this指向对象

- 继承时二选一就可

  - apply传递的是this和以数组形式

  - call传递的是单个的值

  - ```javascript
    Person.apply(this, [name, age]);
    Person.call(this, name, age);
    ```

##### 原型链  

- 原型propotype 

- ```javascript
  //使用new创建对象执行了那几步
  //1.创建一个对象
  //属性—__proto__，指向了构造函数的原型
  //2.将this指向这个对象
  //3.执行构造函数
  //4.返回这个对象
  var p = new Person();
  
  p.sayHello();
  
  //当访问一定一个对象的属性的时候，首先在这个对象本身进行查找
  //如果找到，就直接返回这个属性，且停止查找
  //如果没找到，会继续在原型上找，也就是__proto__指向的那个对象
  ```

##### 混合继承

- 属性放到对象上，方法放到原型上	

- 属性既不会子类或者某个对象给改变，也保证了所有的函数能被所以的对象所共享

- ```javascript
      function Person(name, age) {
          this.name = nmae;
          this.age = age;
      }
      Person.prototype.sayHello = function() {
          alert(this.name);
      }
    
      function Student(name, age, id) {
          Person.apply(this, [name, age]);
          this.id = id;
      }
    
      Student.prototype = Object.create(Person.prototype);
      Student.prototype.study = function() {
    
      }
  ```

  

### 简单数据类型和复杂数据类型

#### 简单数据类型

- 值类型：在存储时变量中存在的是值的本身，如：string，number，boolean，undefined，null
- null返回的是一个空的对象object，如果忧国变量我们以后打算存储为对象，但没想好放啥，这个时候就给null
- 放到栈

#### 复杂数据类型（引用类型）

- 在存储变量中存储的仅仅是地址（引用）
- 通过new关键字创建的对象（系统对象、自定义对象），如Object、Array、Date等
- 放到堆

### DOM

#### 简介

##### DOM树

- 文档：一个页面就是一个文档，DOM中使用document表示
- 元素：页面中的所有标签都是元素，DOM中使用element表示
- 节点：网页中的所有内容都是节点（标签、属性、文本、注释等），DOM中使用node表示
- DOM把以上元素都看成对象

#### 获取页面元素

##### 根据ID获取

- ```JavaScript
  <div id="time">2019-9-9</div>
  <script>
      var timer =document.getElementById('time');
  	console.log(timer);
  	console.log(typeof timer);
  	console.dir(timer);
  </script>
  ```

- 注意：

  1. 因为我们文档页面从上往下加载，所以先得有标签，所以我们script写到标签的下面
  2. get 获得element 元素by通过        驼峰命名法      getElementById
  3. 参数id是大小写敏感的字符串
  4. 返回的是一个元素对象
  5. console.dir()打印我们返回的元素对象  更好的查看里面的属性和方法

##### 根据标签名获取

- 使用getElementsByTagName()方法可以返回带有指定标签名的**对象的集合**

- ```javascript
  document.getElementsByTagName('标签名');
  ```

- 注意：

  1. 因为得到的是一个对象的集合，以伪数组的形式存储的，所以我们想要操作里面的元素就需要遍历
  2. 得到元素对象是动态的
  3. 如果页面中只有一个此标签，返回的还是伪数组的形式
  4. 如果页面中没有此标签，返回的是空的伪数组的形式

##### 通过HTML5新增的方法获取(类名)

- ```javascript
  var dox1=document.getElementsByClassName('类名');
  ```

  - 返回的也是伪数组

- ```javascript
  var firstBox=document.querySelector('选择器');
  ```

  - 返回指定选择器的第一个元素对象
  - 选择器必须要加符号

- ```javascript
  var AlltBox=document.querySelectorAll('选择器');
  ```

  - 返回指定选择器的所有元素对象集合
  - 选择器必须要加符号

##### 获取特殊元素

###### 获取body元素

```javascript
doucument.body//返回body元素对象
```

###### 获取html元素

```javascript
doucument.doucumentElement//返回html元素对象
```

##### window.getComputedStyle()

- `Window.getComputedStyle()`方法返回一个对象，该对象在应用活动样式表并解析这些值可能包含的任何基本计算后报告元素的所有CSS属性的值。 私有的CSS属性值可以通过对象提供的API或通过简单地使用CSS属性名称进行索引来访问。

- 语法

  ```javascript
  let style = window.getComputedStyle(element, [pseudoElt]);
  ```

- element

  用于获取计算样式的[`Element`](https://developer.mozilla.org/zh-CN/docs/Web/API/Element)。

- pseudoElt 可选

  指定一个要匹配的伪元素的字符串。必须对普通元素省略（或`null`）。

- 返回的`style`是一个实时的 [`CSSStyleDeclaration`](https://developer.mozilla.org/zh-CN/docs/Web/API/CSSStyleDeclaration) 对象，当元素的样式更改时，它会自动更新本身。

#### 事件基础

触发---响应机制

##### 事件三元素

1. 事件源

- 事件被触发的对象

2. 事件类型

   - 如何触发 什么事件 比如：鼠标点击（onclick）还是鼠标经过还是键盘按下
3. 事件处理程序

- 通过一个函数赋值的方式完成

4. 例：

   ```javascript
   <button id="btn">唐伯虎</button>
   <script>
   	var btn = domcument.getElementById('btn');
   	btn.onclick = function() {
       	alart('点秋香');
   	}
   </script>
   ```

##### 执行事件的步骤

1. 获取事件源
2. 注册事件（绑定事件）
3. 添加事件处理程序（采用函数赋值形式）

#### 操作元素

##### 改变元素的内容

- 从起始位置到终止位置的内容，但他去除一个html标签，同时空格和换行也会去掉

  ```javascript
  element.innerText
  ```

- 起始位置到终止位置的全部内容，包括html标签，同时保留空格和换行

  ```javascript
  element.innerHTML
  ```

- 区别：

  1. innerText不能识别HTML标签   分标准         去除空格和换行

  2. innerHTML能识别HTML标签   W3C标准      保留空格和换行

  3. 这两个属性都是可读写的 可以获取元素

     ```javascript
     var p = document.querySelector('p');
     console.log(p.innerText);
     ```


##### 常用元素的属性操作

```javascript
1. innerText 、innerHTML   改变元素内容
2. src 、herf
3. id、alt、title
```

##### 表单元素的属性操作

```javascript
type、value、checked、selected、disabled
```

##### 样式属性操作

- 我们可以通过JS修改元素的大小、颜色、位置等样式

- ```javascript
  element.style       //行内样式操作
  element.className   //类名样式操作
  ```

- 里面的样式采用驼峰命名法

- Js修改style样式操作，产生的是行内样式，CSS权重比较高

- 注意：

  1. 如果样式修改较多，可以采用操作类名方式更改元素样式
  2. class因为是个保留字，因此使用className来操作元素类名属性
  3. className会直接更改元素的类名，会覆盖原来的类名

- ```javascript
  <style>
          div {
              width: 100px;
              height: 100px;
              background-color: pink;
          }
          
          .change {
              background-color: purple;
              color: #fff;
              font-size: 25px;
              margin-top: 100px;
          }
      </style>
  
  <body>
      <div class="first">文本</div>
      <script>
          // 1. 使用 element.style 获得修改元素样式  如果样式比较少 或者 功能简单的情况下使用
          var test = document.querySelector('div');
          test.onclick = function() {
              // this.style.backgroundColor = 'purple';
              // this.style.color = '#fff';
              // this.style.fontSize = '25px';
              // this.style.marginTop = '100px';
              // 让我们当前元素的类名改为了 change
  
              // 2. 我们可以通过 修改元素的className更改元素的样式 适合于样式较多或者功能复杂的情况
              // 3. 如果想要保留原先的类名，我们可以这么做 多类名选择器
              // this.className = 'change';
              this.className = 'first change';
          }
      </script>
  </body>
  ```


##### 排它思想

```javascript
<button>按钮1</button>
<button>按钮2</button>
<button>按钮3</button>
<button>按钮4</button>
<button>按钮5</button>
<script>
    // 1. 获取所有按钮元素
    var btns = document.getElementsByTagName('button');
    // btns得到的是伪数组  里面的每一个元素 btns[i]
    for (var i = 0; i < btns.length; i++) {
        btns[i].onclick = function() {
        // (1) 我们先把所有的按钮背景颜色去掉  干掉所有人
        for (var i = 0; i < btns.length; i++) {
             btns[i].style.backgroundColor = '';
         }
        // (2) 然后才让当前的元素背景颜色为pink 留下我自己
         this.style.backgroundColor = 'pink';

        }
     }
//2. 首先先排除其他人，然后才设置自己的样式 这种排除其他人的思想我们成为排他思想
    </script>
```

##### 自定义属性的操作

- 目的：是为了保存并使用数据，有些数据可以保存到页面而不用保存到数据库中

- 获取属性值
  1. element.属性         获取属性值
  2. element.getAttribute('属性');

- 区别
  1. element.属性            获取内置属性值（元素本身自带的属性）
  2. element.getAttribute('属性');主要获得自定义的属性（标准）我们程序员自定义的属性    自定义属性如：index="1"；

- 设置属性值
  1. element.属性='值';         设置内置属性值
  2. element.setAttribute('属性','值');//主要针对于自定义属性，也可以设置其他的属性，class特殊，这里面就写class，不是className

- 移除属性

1. element.removeAttribute('属性');

- H5自定义属性

  1. 设置

     - H5规定自定义属性data开头作为属性名并且赋值

     - 比如<div data-index="1"></div>或者使用JS设置

       element.setAttribute('data-index',2)

  2. 获取

     - 兼容性获取element.getAttribute('data-index')
     - H5新增element.dataset.index或者element.dataset['index']   ie11才开始支持
     - 如果自定义属性里面有多个-链接的单词，我们获取的时候采取*驼峰命名法*

#### 节点操作

##### 原因

- 利用DOM提供的方法逻辑性不强、繁琐
- 使用节点层级关系获取元素
  - 利用父子节点关系获取元素
  - 逻辑性强、但兼容性稍差

##### 节点概述

- 一般的节点有三个基本属性
  - 节点类型：nodeType
    1. 元素节点   1
    2. 属性节点    2
    3. 文本节点    3（文本节点包括文字、空格、换行等）
  - 节点名称：nodeName
  - 节点值：nodeValue

##### 节点层级

- 父子兄层级关系

  1. 父级节点

     - ```javascript
       node.parentNode
       ```

     - parentNode属性可返回某节点的父节点，注意是最近的一个父节点

     - 如果指定的节点没有父节点则返回null

  2. 子节点

     ```javascript
     1.parentNode.childNodes(标准)
     ```

     - parentNode.childNodes返回包含指定节点的子节点的集合（元素节点、文本节点），该集合为及时更新的集合
     - 换行是文本节点
     - 如果想要获得里面的元素节点，就需要专门处理，所以我们一般不提倡使用childNodes

     ```javascript
     var ul = document.querySelector('ul');
     for(var i = 0;i<ul.childNodes.length;i++){
         if(ul.childNodes[i].nodeType == 1){
             //ul.childNodes[i]是元素节点
             console.log(ul.childNodes[i]);
         }
     }
     ```

     ```javascript
     2.parentNode.children(非标准)
     ```

     - parentNode.children是一个只读属性，返回所有的子元素节点，他只会返回子元素的节点。他只会返回子元素的节点，其余节点，其余节点不返回（这是我们重点掌握的）
     - 虽然children是一个非标准，但得到了各个浏览器的支持，因此我门可以放心使用

     ```javascript
     3.parentNode.firstChild
     ```

     - firstChild返回第一个子节点，找不到则返回null。同样，也是包含所有的节点

     ```javascript
     4.parentNode.lastChild
     ```

     - lastChild返回第一个子节点，找不到则返回null。同样，也是包含所有的节点

     ```javascript
     5.parentNode.firstElemenChild
     ```

     - firstElemenChild返回第一个子元素节点，找不到则返回null

     ```javascript
     6,parentNode.lastElemenChild
     ```

     - lastElemenChild返回第一个子元素节点，找不到则返回nul
     - **注意：这两个方法有兼容性问题，IE9以上才支持**

     ```javascript
     7. children[0]     //返回第一个元素
     8. ol.chiildren[ol.children.length-1]
     ```

     - 实际写法，既没有兼容性问题还可以返回第一个和最后一个元素

  3. 兄弟节点

     1. ```javascript
        node.nextSibling
        ```

        nextSibling返回当前元素的下一个兄弟节点，找不到则返回null。同样，也包含所有节点（文本节点、元素节点等等）

     2. ```javascript
        node.previousSibling
        ```

        previousSibling返回当前元素上一个兄弟节点，找不到则返回null。同样，也包含所有的节点（文本节点、元素节点等等）

     3. ```javascript
        node.nextElementSibling
        ```

        nextElementSibling返回当前元素下一个兄弟元素节点，找不到则返回null

     4. ```javascript
        node.previouslementSibling
        ```

        previouslementSibling返回当前元素下一个兄弟元素节点，找不到则返回null

        **注意：这3.4方法有兼容性问题，IE9以上才支持**

     5. 解决方法

        ```javascript
        function getNextElementSibling(element) {
            var el = element;
            while (el = el.nextSibling) {
                if(el.nodeType == 1){
                    return el;
                }
            }
            return null;
        }
        ```

##### 创建节点

- ```javascript
  document.createElement('tagName')
  ```

- document.createElement()方法创建由tagName指定的HTML元素 。因为这些元素原来不存在，是根据我们的需求动态生成的，所以我们也称为动态创建元素节点

##### 添加节点

- ```javascript
  node.appendChild(child)
  ```

  node.appendChild()方法将一个节点添加到指定父节点的子节点列表的末尾。类似于CSS里面的after伪元素

- ```javascript
  node.insertBefore(child,指定元素)
  ```

  node.insertBefore(child,指定元素)    方法将一个节点添加到指定父节点的子节点列表的前面

##### 删除节点

- ```javascript
  node.removeChild(child)
  ```

  node.removeChild()方法从DOM中删除一个子节点，返回删除的节点

- ```javascript
  	// 1.获取元素
         var ul = document.querySelector('ul');
         var btn = document.querySelector('button');
         // 2. 删除元素  node.removeChild(child)
         // ul.removeChild(ul.children[0]);
         // 3. 点击按钮依次删除里面的孩子
   		//小技巧:当li删除完之后禁用删除键	
         btn.onclick = function() {
             if (ul.children.length == 0) {
                 this.disabled = true;//禁用删除键
             } else {
                 ul.removeChild(ul.children[0]);
             }
         }
  ```


##### for   in 复习

```javascript
 for(var k in obj) {
//     k 得到的是属性名
//     obj[k] 得到是属性值
// }
```

##### 三种动态串创建元素的区别

- document.write()

  - 创建元素 如果页面文档流加载完毕，在调用这句话会导致页面重绘

- element.innerHTNL

  - innerHTML 是将内容写入某个DOM节点，不会导致页面全部重绘

  - innerHTML创建多个元素效率更高（不要拼接字符串，采用数组的形式拼接），结构稍微复杂

  - ```javascript
    function fn(){
        var array=[];
        for(var i=0;i<1000;i++){
            array.push('<div></div>');
        }
        document.body.innerHTML=array.join('');
    }          
    ```

- document.createElement()

  - createElement()创建多个元素效率稍微低低一点点，但结构更清晰

#### DOM重点核心

#### 事件高级导读

##### 注册事件（绑定属性）

###### 概述

- 注册事件分为两种：传统方式和方法监听注册

- | 传统注册方式                                                 | 方法监听注册方式                                 |
  | ------------------------------------------------------------ | ------------------------------------------------ |
  | 利用on开头的事件onclick                                      | W3C标准  推荐方式                                |
  | <button onclick='alart("hi~")'></button>                     | addEventListener()它是一个方法                   |
  | btn.onclick=function(){}                                     | IE9之前的IE不支持此方法，可使用attackEvent()代替 |
  | 特点：注册事件的唯一性                                       | 特点：同一个元素同一个事件可以注册多个监听器     |
  | 同一个元素同一个事件只能设置一个处理函数，最后注册的处理函数将会覆盖前面注册的处理函数 |                                                  |

###### addEventListener事件监听方式

- ```javascript
  eventTarget.addEventListener(type,listener[,useCapturel])
  ```

- eventTarget.addEventListener()方法将指定的监听器注册到eventTarge(目标对象)上，当该对象触发指定的事件是，就会执行事件处理函数

- 该方法接受三个参数：

  1. type：事件类型字符串，比如click、mouseover，注意这里不要带on
  2. listener：事件处理函数，事件发生时，会调用该监听函数
  3. useCapture:可选参数，是一个布尔值，默认值是false，学完DOM事件流后，我们在进一步学习

- I9以上支持

- 事件处理函数，如果写函数名的话，不用加（）

- useCapture:

  1. 为 true 时：处于捕获阶段
  2. 为false 或者  省略  时：处于冒泡阶段

###### attachEvent事件监听方式

- 非标准，不建议使用，I9以前版本执行，了解知道

- ```javascript
  eventTarget.attachEvent(eventNameWithOn,callback)
  ```

- eventTarget.attachEvent()方法将指定的监听器注册到eventTarge（目标对象）上，当该对象触发指定的事件时，指定的回调函数就会被执行

- 该方法接受两个参数

  - eventNameWithOn:事件类型字符串，比如onclick、onmouseover,这里要带on
  - callback：事件处理函数，当目标触发事件的时回调函数被调用

##### 删除事件

- 传统注册方式
  - eventTarget.onclick=null;

- 方法监听注册方式
  - eventTarget.removeEventListner(type,Listner[,useCapture]);
  - eventTarget.datachEvent(eventNameWithOn,callback);
    - eventNameWithOn这里要带on

##### DOM事件流

- 事件流描述的是从页面中接受事件的顺序
- 事件发生时会在元素节点之间按照特定的顺序传播，这传播过程即DOM事件流
- DOM事件流分为3个阶段
  1. 捕获阶段
  2. 当前目标阶段
  3. 冒泡阶段

- 事件冒泡：IE最早提出，事件开始时由具体的元素接受，然后逐级向上传播到DOM最顶层节点的过程
  - onblur、onfocus、onmouseenter、onmouseleave是没有冒泡的
- 事件捕获：网易最早提出，由DOM最顶层节点开始，然后逐级向下传播到具体的元素接受的过程

##### 事件对象

- ```javascript
  div.onclick=function(event){
      
  }
  div.addEventListener('click',function(event){
    
  })
  ```

- event 就是一个事件对象，写到我们我们监听函数的小括号里面 当形参来看

- 事件对象只有有了是事件才会存在，他是系统给我们自动创建的，不需要我们传递参数

- 事件对象是我们事件的一系列相关数据的集合跟集合相关的，比如鼠标点击里面就包含了鼠标的相关信息，

- 事件对象可以自己命名，比如event、evt、e

- 事件对象也有兼容性问题IE678通过window.event

- 兼容性处理

  ```javascript
  div.onclick=function(e){
      //console.log(e);
      //console.log(window.event);
      e=e||window.event;
      console.log(e);
  }
  ```

- 当我们注册事件时，event对象就会被系统自动创建，并依次传递给事件监听器（事件处理函数）

- 常用属性方法：

  | 事件对象属性方法    | 说明                                                         |
  | ------------------- | ------------------------------------------------------------ |
  | e.target            | 返回触发事件的对象           标准                            |
  | e.srcElement        | 返回触发事件的对象            非标准ie6·8使用                |
  | e.type              | 返回事件的类型，比如click、mouserover不带on                  |
  | e.cancelBubble      | 该属性组织冒泡，非标准ie6·8使用                              |
  | e.returnValue       | 该属性阻止默认事件（默认行为）非标准ie6·8使用比如不让链接跳转 |
  | e.preventDafault()  | 该方法阻止默认事件（默认行为）标准 不让链接跳转              |
  | e.stopPropagation() | 阻止冒泡标准                                                 |

  - e.target  返回**触发**事件的对象   this返回的是**绑定**事件的对象（元素）
  - 了解：跟this有个非常相似的属性currentTarget   ie678不认识
  - return false也能组织默认行为，且没有兼容性问题，**return后面的代码不执行了**而且只限于传统注册方式

##### 阻止事件冒泡

###### 标准写法

- 利用事件对象里面的stopPropagation()方法   stop停止 Propagation传播

  ```javascript
  e.stopPropagation()
  ```

###### 非标准写法

- IE6-8利用事件对象cancelBubble属性

  ```javascript
  e.cancelBubble = true;
  ```

  cancel  取消   bubble泡泡

######  兼容性解决方案

- ```javascript
  if(e && e.stopPropagation){
      e.stopPropagation();
  }else{
      window.event.cancelBubble = true;
  }
  ```

##### 事件委托

- 事件委托
  - 事件委托也称为事件代理，在jQuery里面被称为事件委派

- 事件委托的原理
  - 不是每个子节点单独设置事件监听器，而且事件监听器设置在其父节点上，然后利用冒泡原理影响设置每个子节点

#### 常用的鼠标事件

| 鼠标事件    | 触发条件                                                   |
| :---------- | ---------------------------------------------------------- |
| onclick     | 鼠标点击左键触发                                           |
| onmouseover | 鼠标经过触发                                               |
| onmouseout  | 鼠标离开触发                                               |
| onfocus     | 获得鼠标焦点触发                                           |
| onblur      | 失去鼠标焦点触发                                           |
| onmousemove | 鼠标移动触发                                               |
| onmouseup   | 鼠标弹去触发                                               |
| onmousedown | 鼠标按下触发                                               |
| mouseleave  | 鼠标离开，不会冒泡，和mouseenter搭配                       |
| mouseenter  | 当鼠标移动到元素上就触发，不过只经过自身盒子触发，不会冒泡 |
| mouseover   | 鼠标经过自身盒子和子盒子会触发                             |

- 禁止鼠标右键菜单

  - contextmenu主要控制应该何时显示上下文菜单，主要用于程序员取消默认的上下文菜单

  - ```javascript
    document.addEventListener('contextmenu',function(e){
        e.preventDefault();
    })
    ```

- 禁止鼠标选中

  - selectstart开始选中

  - ```javascript
    document.addEventListener('selectstart',function(e){
        e.preventDefault();
    })
    ```

###### 鼠标事件对象

- event对象代表事件的状态，跟事件相关的一系列信息的集合，现阶段我们主要是用鼠标事件对象MouseEvent和键盘对象KeyboardEvent

- | 鼠标事件对象 | 说明                                                      |
  | ------------ | --------------------------------------------------------- |
  | e.clientX    | 返回鼠标相对于浏览器窗口可视区的X坐标，不随页面滚动而变化 |
  | e.clientY    | 返回鼠标相对于浏览器窗口可视区的Y坐标                     |
  | e.pageX      | 返回鼠标相对于文档页面的X坐标  IE9+支持                   |
  | e.pageY      | 返回鼠标相对于文档页面的Y坐标  IE9+支持                   |
  | e.screenX    | 返回鼠标相对于电脑屏幕的X坐标                             |
  | e.screenY    | 返回鼠标相对于电脑屏幕的Y坐标                             |

#### 常用的键盘事件

| 键盘事件   | 触发条件                                                     |
| ---------- | ------------------------------------------------------------ |
| onkeyup    | 某个键盘按键被松开时触发                                     |
| onkeydown  | 某个键盘按键被按下时触发                                     |
| onkeypress | 某个键盘按键被按下时触发，但是它不识别功能键，比如ctrl shift 箭头等 |

-  注意：三个事件的执行顺序是onkeydown----onkeypress----onkeyup
-  keydown：当用户按下键盘上的任意键时触发，如果按住不放的话，会重复触发此事件；
-  keypress：当用户按下键盘上的**字符键**时触发，如果按住不让的话，会重复触发此事件；
-  keyup：当用户**释放**键盘上的字符键时触发。

##### 键盘事件对象

| 键盘事件对象属性 | 说明              |
| ---------------- | ----------------- |
| keyCode          | 返回该键的ASCll值 |

- 我们的keyup和keydown事件不区分大小写  a和 A得到的都是65
- 我们的keypress事件区分大小写 
- 利用keyCode返回的ASCll码判断按下的是那个键
- 属性：
  - element.altKey    element.strlKey    element.shiftKey

### BOM

#### BOM概述

##### 什么是BOM

- BOM即浏览器对象模型，他提供了独立于内容而与浏览器窗口进行交会的对象，其核心对象是window
- BOM由一系列相关的对象有关，并且每个对象都提供了而很多的方法和属性

- BOM是将浏览器看作一个对象来看待的
- BOM由个浏览器厂商在各自浏览器上定义的，兼容性较差

##### BOM的构成

- window对象是浏览器的顶级窗口，它具有双重角色
  1. 他是JS访问浏览器窗口的一个接口
  2. 他是一个全局对象，定义在全局作用域中的变量，函数会变成window对象的属性和方法
  3. 调用的时候可以省略window，前面学习的对话框都属于window对象方法，如alart()、prompt()等
  4. 注意：window下一个特殊属性是window.name

#### window对象的常见事件

##### 窗口加载事件

###### load

- ```javascript
  window.onload = function(){}
  //或者
  window.addEventListener("load"，function(){});
  ```

- window.onload是窗口（页面）加载事件，当文档内容完全加载完成会触发该事件（包括图像、脚本文档、CSS文件等），就调用的处理函数

- 注意：

  1. 有了window.onload就可以吧JS代码写到页面元素的上方，因为onload是等页面内容全部加载完毕，再去执行处理函数
  2. window.onload传统注册事件的方式只能写一次，如果有多个，以最后一个为准
  3. 如果使用addEventListener，则没有限制

###### DOMContentLoaded

- ```javascript
  domcument.addEventListener('DOMContentLoaded',function(){})
  ```

- DOMContentLoaded事件触发时，仅当DOM加载完成，不包括样式表，图片，flash等等 IE以上才支持

- 如果页面的图片很多的话，从用户访问到onload触发可能需要较长的时间，交互效果就不能实现，必然影响用户体验，此时用DOMContentLoaded事件比较合适

- 区别：

  - load是等页面内容全部加载完毕，再去执行处理函数
  - DOMContentLoaded是DOM加载完毕，不包含图片、falsh css等就可以执行

##### 调整窗口大小事件

- ```javascript
  window.onresize = function(){};
  window.addEventListener('resize',function(){});
  ```

- window.onresize是调整窗口大小加载事件，当触发时就调用的处理函数

- 注意：

  1. 只要窗口大小像素发生变化，就会触发整个事件
  2. 我们经常利用这个事件完成响应式布局，window.innerWidth当前屏幕的宽度

#### 定时器

##### 两种定时器

1. setTimeout()    

   - ```javascript
     window.setTimeout(调用函数,[延迟的毫秒数]);         
     ```

   - setTimeout()方法用于设置一个定时器，该定时器在**定时器到期后执行调用函数**

   - 调用函数可以直接写函数也可以写函数名

   - 这个调用函数，需要等待时间，时间到了才会去调用这个函数，因此称为**回调函数**。简单理解，回调就是回头调用的意思，下一件干完，再回头调用这个函数

   - 延迟的毫秒数省略默认是0，如果写，必须是毫秒

   - ```javascript
     function callback(){
         
     }
     setTimeout(callback,3000);
      setTimeout('callback()',3000);//不提倡
     ```

2. 停止setTimeout()定时器

   - window.clearTimeout(timeoutID)

   - ```javascript
     <button>点击停止</button>
         <script>
             var btn = document.querySelector('button');
             var timer = setTimeout(function() {
                 console.log('爆炸了');
             }, 3000);
             btn.addEventListener('click', function() {
                 clearTimeout(timer);
             })
         </script>
     ```

3. setInterval()定时器

   - ```javascript
     window.setlnterval(回调函数,[间隔的毫秒数]);
     ```

   - setInterval()方法**重复调用一个函数**，每隔一个函数，每隔这个时间，就去调用一次回调函数

   - 注意：

     1. window可以省略
     2. 这个调用函数可以直接写函数，或者写函数名或者采取字符串'函数名()'三种形式
     3. 间隔的毫秒数默认为0，如果写，必须是毫秒，表示每隔多少毫秒就自动调用这个函数
     4. 因为定时器可能有很多，所以我们经常给定时器赋值一个标识符

4. 停止setInterval()定时器

   - ```javascript
     window.clearInterval(intervalID);
     ```

   - clearInterval()方法取消了先前通过调用setInterval()建立的定时器

   - 注意：

     1. window可以省略
     2. 里面的参数就是定时器的标识符


#### this指向问题

- this的指向在函数定义的时候是确定不了的，只要在函数执行的时候才能确定this到底指向谁，一般情况this的最终指向的是那个调用它的对象
- 在全局作用域或者普通函数中this的指向全局对象window（注意定时器里面的this指向window）
- 方法调用中谁调用this指向谁
- 构造函数中this指向构造函数的实例
- 定时器里面的this指向window

#### JS执行机制

##### JS是单线程

- JS最大的特点是单线程，同一时间只能做一件事
- 若JS执行时间过长，这样就会造成页面渲染不连贯，导致页面渲染加载阻塞的感觉

##### 同步和异步

为了解决这个问题，利用多核CPU的计算能力

###### 同步

前一个任务结束后再去执行后一个任务，程序的执行顺序于任务排列顺序是一致的、同步的，比如做饭的同步做法：我们要烧水做饭，等水开了（十分种后），再去切菜、炒菜

###### 异步

你在做一件事时，因为这件事会花费很长时间，在做这件事的同时，你还可以去处理其他事，比如做饭的异步做法，我们在烧水的同时，利用这10分钟，去切菜，炒菜

###### 本质区别

这条流水线上各个流程的执行顺序不同

###### 同步任务

同步任务都在主线程上执行，形成一个执行栈

###### 异步任务

- JS异步是通过回调函数实现的
- 一般而言，异步任务有以下三种类型
  1. 普通事件，如click、resize
  2. 资源加载，如load、error
  3. 定时器，包括setInterval、setTimeout

- 异步任务相关回调函数添加到任务列表中（任务队列也称为消息队列）

##### JS执行机制

- 先执行执行栈中的同步任务
- 异步任务（回调函数）放在任务队列
- 一旦执行栈中的所有同步任务执行完毕，系统会按次序读取任务队列中的异步任务，于是被读取的异步任务结束等待状态，进入执行栈，开始执行

#### open对象

- window.open()    &open()

- 内容：

  1. 加载URL
  2. 窗口的名称或者窗口的目标
  3. 一串具有特殊意义的字符串

- 注：

  - 如果只有第一个参数，调用open方法会打开新窗口，加载url

  - 第二个参数，是给打开的新窗口起一个名字然后以后，再去加载url

  - 第三个参数是字符串

    - | 名称   | 值   | 说明                      |
      | ------ | ---- | ------------------------- |
      | width  | 数值 | 新窗口的宽度，不能小于100 |
      | height | 数值 | 新窗口的高度，不能小于100 |
      | top    | 数值 | 新窗口的Y坐标，不能是负值 |
      | left   | 数值 | 新窗口的X坐标，不能是负值 |

    - 设置当前打开窗口的参数

  - opener是打开当前窗口的父窗口的window对象(**IE不支持**)

#### location对象

window对象给我们提供了一个location属性用于获取或设置窗体的URL，并且可以用于解析URL。因为这个属性返回的是一个对象，我们将这个属性也成为location对象

###### URL

- 统一资源定位符是互联网上标准资源的地址。互联网上的每个文件都有唯一的URL，它包含的信息指出文件的位置以及浏览器应该怎么处理它

- 一般语法格式

  ```
  protocol://host[:post]/path/[?quary]#fragmrnt
  http://www.itcast.cn/index.html?name=andy&age=18#link
  ```

| 组成     | 说明                                                         |
| -------- | ------------------------------------------------------------ |
| protocol | 通信协议 常用的http,ftp,maito等                              |
| host     | 主机（域名）www.itheima.com                                  |
| port     | 端口号 可选，省略时使用方案的默认接口，如http的默认端口为80  |
| path     | 路径 由 零或多个'/'符号隔开的字符串，一般用来表示主机上的一个目录或文件地址 |
| query    | 参数 以键值对的形式，通过&符号分隔开                         |
| fragment | 片段  #后面的内容常用于链接 锚点                             |

###### location对象属性

| location对象属性    | 返回值                               |
| ------------------- | ------------------------------------ |
| location.herf       | 获取或着设置整个URL                  |
| location.host       | 返回主机（域名）www.itheima.com      |
| location.port       | 返回端口号 如果未写返回空字符串      |
| falocation.pathname | 返回路径                             |
| location.search     | 返回参数                             |
| location.hash       | 返回片段 #后面的内容 常见于链接 锚点 |

- 给location.href赋值，可以跳转到其他页面
- window.location==window.document.location

###### location常见方法

- | location对象方法   | 返回值                                                       |
  | ------------------ | ------------------------------------------------------------ |
  | location.assign()  | 跟href一样，可以跳转页面（也称重定向页面）                   |
  | location.replace() | 替换当前页面，因为不记录历史，所以不能后退页面               |
  | location.reload()  | 重新加载页面，相当于刷新按钮或者f5,如果参数为true强制刷新ctrl+f5 |


#### nevigator对象

- navigator对象吧包含有关浏览器的信息，他有很多属性，我们最常用的是userAgent，该属性可以返回由客户机发送服务器的user-agent头部的值

- 下面前端代码可以判断用户那个终端打开页面，实现跳转

  ```
  if((navigator.userAgent.match(/(phone|pad|pod|iphone|ipod|ios|ipad|Android|Mobile|BlackBeery|IEMobile|MQQBrowser|JUC|Fennec|wOSBrowser|BrowserNG|Webos|Symbian|window Phone)/i))) {
  	window.location.href = "";//手机
  }else {
  	window.location.href = "";//电脑
  }
  ```

#### history对象

- window对象给我们提供了一个history对象，与浏览器历史记录进行交互，该对象包含用户（在浏览器窗口中）访问过的URL

- | history对象方法 | 作用                                                    |
  | --------------- | ------------------------------------------------------- |
  | back()          | 可以后退功能                                            |
  | forward()       | 前进功能                                                |
  | go(参数)        | 前进后退功能 参数如果是1前进1个页面如果是-1后退一个页面 |

#### search处理

- search.indexOf(key)//找不到目标返回值就是-1

### PC端网络特效

#### 元素偏移量offset系列

##### offset概述

- offset翻译过来就是偏移量，我们使用offset系列相关属性可以动态的得到该元素的位置（偏移）、大小等

  - 获得元素距离带有定位父元素的位置
  - 获得元素自身大小（宽度高度）
  - 注意：返回的数值不带单位

- offset系列常用属性：

  | offset系列属性       | 作用                                                         |
  | -------------------- | ------------------------------------------------------------ |
  | element.offsetParent | 返回作为该元素带有定位的父级元素 如果父级元素都没有定位则返回body |
  | element.offsetTop    | 返回元素相对带有定位父元素上方的偏移                         |
  | element.offsetLeft   | 返回元素相对带有定位元素左边框的偏移                         |
  | element.offsetWidth  | 返回自身包括padding、边框、内容区的高度，返回数值不带单位    |
  | element.offsetHeight | 返回自身包括padding、边框、内容区的高度，返回数值不带单位    |

##### offset与style区别

- offset
  - offset可以得到任意样式表中的样式值
  - offset系列获得的数值是没有单位的
  - offsetWidth包含padding+border+width
  - offsetWidthde等属性是只读属性，只能获取不能赋值
  - 所以，我们想要获取元素大小位置，用offset更合适

- style
  - style只能得到行内样式表中的样式值
  - style.width获得的是带单位的字符串
  - style.widyh获得不包含padding和border的值
  - style.width是可读写属性，可以获取也可以赋值
  - 所以，我们想要给元素更改值，则需要用style改变

#### 元素可视区client系列

- client翻译过来就是客户端，我们使用client系列的相关信息，通过client系列的相关属性可以动态的得到该元素的边框大小，元素大小等。

- | client系列属性       | 作用                                                         |
  | -------------------- | ------------------------------------------------------------ |
  | element.clientTop    | 返回元素的上边框的大小                                       |
  | element.clientLeft   | 返回元素左边框的的大小                                       |
  | element.clientWidth  | 返回自身包括padding，内容区的宽度，不含边框，返回数值不带单位 |
  | element.clientHeight | 返回自身包括padding，内容区的高度，不含边框，返回数值不带单位 |

##### 立即执行函数

- 定义：不需要带哦有，立马能够自己执行的函数

- 写法：(function () {} ) ()     或者       （function () {} () );
- 主要作用：创建一个独立的作用域0，避免命名冲突问题
- 第二个小括号可以看作是调用函数
- 也可以写函数名

#### 元素滚动sroll系列

##### 元素sroll系列属性

- sroll翻译过来就是滚动的，我们使用sroll系列的相关属性可以动态的得到该元素的大小，滚动距离等

- | sroll系列属性       | 作用                                           |
  | ------------------- | ---------------------------------------------- |
  | element.srollTop    | 返回被卷去的上侧距离，返回数值不带单位         |
  | element.srollLeft   | 返回被卷去的左侧距离，返回数值不带单位         |
  | element.srollWidth  | 返回自身的实际宽度，不含边框，返回数值不带单位 |
  | element.srollHeight | 返回自身的实际高度，不含边框，返回数值不带单位 |

##### 页面被卷去 的头部兼容性解决方案

- 需要注意的是，页面被卷去的头部，有兼容性问题，因此被卷去的头部通常有以下几种写法

  1. 声明了DTD，使用document.documentElement.scrollTop
  2. 未声明DTD，使用document.body.srollTop
  3. 新方法window.pageYOffset和window.pageXOffset,IE9开始 支持

- ```javascript
  function getScroll(){
  	return {       				left:window.pageXOffset||document.documentElement.scrollLeft||document.body.srollLeft||0,
  top:window.pageYOffset||document.documentElement.scrollTop||document.body.srollTop||0
      };
  }
  //使用的时候 
  getSroll().left
  ```

#### 三大系类总结

| 三大系列大小对比    | 作用                                                         |
| ------------------- | ------------------------------------------------------------ |
| element.offsetWidth | 返回自身包括padding，边框，内容区的高度，返回数值不带单位    |
| element.clientWidth | 返回自身包含padding，内容区的宽度，不含边框，返回数值不带单位 |
| element.srollWidth  | 返回自身实际的宽度，不含边框，返回数值不带单位               |

- 主要用法
  1. offset系列经常用于获得元素位置 offsetLeft、ofFsetTop
  2. client经常用于获取元素大小clientWidth、clientHeight
  3. scroll经常用于获取滚动距离scrollTop、scrollLeft
  4. 注意页面滚动距离通过window.pageXOffset获得

#### 小知识点

##### dpr  物理像素比

- var dpr=window.devicePixelRatio ||  1
- 如果有自身的像素比，如有就用本身的，没有就用1
- PC端是1
- iphone678是2

##### pageshow事件

- 我们重新加载页面触发的事件

- e.persisted 返回的是true 就是说如果这个页面是从缓存取过来的页面，也需要重新计算一下rem的大小

#### 动画函数封装

##### 动画实现原理

- 核心原理：通过定时器setInterval()不断移动盒子的位置

- ```javascript
  //动画函数的封装
  // 简单动画函数封装obj目标对象 target 目标位置
  function animate(obj, target) {
      //给不同元素指定了不同的定时器
              obj.timer = setInterval(function() {
                  if (obj.offsetLeft >= target) {
                      // 停止动画 本质是停止定时器
                      clearInterval(obj.timer);
                  }
                  obj.style.left = obj.offsetLeft + 1 + 'px';
  
              }, 30);
          }
  ```

##### 缓动效果原理

- 缓动动画就是让元素运动的速度有所变化，最常见的就是让速度慢慢停下来

- 思路：

  1. 让盒子每次移动的距离慢慢减小，速度就会慢慢落下来
  2. 核心算法：(目标值-现在的位置)/10 作为每次移动的距离步长
  3. 停止条件就是：让盒子当前位置等于目标位置就停止定时器

- ```javascript
  function animate(obj, target) {
              // 先清除以前的定时器，只保留当前的一个定时器执行
              clearInterval(obj.timer);
              obj.timer = setInterval(function() {
                  // 步长值写到定时器的里面
                  // 把我们步长值改为整数 不要出现小数的问题
                  // var step = Math.ceil((target - obj.offsetLeft) / 10);
                  var step = (target - obj.offsetLeft) / 10;
                  step = step > 0 ? Math.ceil(step) : Math.floor(step);
                  if (obj.offsetLeft == target) {
                      // 停止动画 本质是停止定时器
                      clearInterval(obj.timer);
                  }
                  // 把每次加1 这个步长值改为一个慢慢变小的值  步长公式：(目标值 - 现在的位置) / 10
                  obj.style.left = obj.offsetLeft + step + 'px';
  
              }, 15);
          }
  ```

##### 动画函数添加回调函数

- 回调函数原理：函数可以作为一个参数，将这个函数作为参数传到另一个函数里面，当那个函数执行完毕之后，再执行传进去的这个函数，这个过程称为**回调**。
- 写到定时器结束里面

##### 节流阀

- 防止轮播图按钮连续点击造成播放太快

- 节流阀目的：当上一个函数动画内容执行完毕，再去执行下一个函数动画，让世界无法连续触发

- 核心实现思路：利用回调函数，添加一个变量来控制，锁住函数和解锁函数

- 开始设置一个变量var flag = true;

- if(flag){

  ​	flag=false;

  ​	do something;

  }//关闭水龙头

- 利用回调函数 动画执行完毕，flag = true 打卡水龙头

### cookie

#### http协议

- HTTP：超文本传输协议，用于从web服务器传输超文本到本地浏览器的传输协议，他是一个无状态的协议

#### cookie概述

- cookie是指缓存在本地客户端的数据

- cookie一般储存100多条数据

- ```javascript
  	//查询cookie
         console.log(document.cookie);
         //设置cookie
         document.cookie = "username=honny";
         //设置存储时间
         var oDate = new Date();
         oDate.setDate(oDate.getDate() + 3);
         document.cookie = "username=honny;expires=" + oDate;
         //修改cookie
         document.cookie = "username=honny";
         document.cookie = "username=honny1";
         //删除cookie
         var oDate = new Date();
         document.cookie = "username=honny;expires=" + oDate;
  ```

#### cookie函数的封装

- 

- ```javascript
  //新建cookie
  function setCookie(name, value, day) {
              var oDate = new Date();
              oDate.setDate(oDate.getDate() + day);
              document.cookie = name + "=" + value + ";expires=" + oDate;
          }
          setCookie("name1", "honney1", 1);
          setCookie("name2", "honney2", 1);
  
          console.log(document.cookie);
  //获取cookie
          function getCookie(name) {
              var str = document.cookie;
              var arr = str.split("; ");
              for (var i = 0; i < arr.length; i++) {
                  var arr1 = arr[i].split("=");
                  if (arr1[0] == name) {
                      return arr1[1];
                  }
              }
          }
  
          console.log(getCookie("name2"));
  //消除cookie
          function removeCookie(name) {
              setCookie(name, 1, -1);
          }
  
          removeCookie("name1");
          console.log(getCookie("name1"));
  ```

### 正则表达式

#### 概念

- 正则表达式是由普通字符及特殊字符组成的对字符串进行过滤的逻辑公式

#### 创建方式

- 字面量的方式

  ```javascript
  var reg = /abc/;
  ```

- 构造函数

  ```javascript
  var reg = new RegExp("abc");
  var str = "ab";
  var flag = reg.test(str);
  ```

  - test方法：正则表达式的方法，用于检测字符串是否含有复合规则的子串，有返回true，没返回false
  - exec方法：正则表达式的方法，将匹配成功的内容放到数组里，如果没有在则返回null
  - match方法：字符串方法 str.match(reg);
  - search方法：用于查找符合规则的子串的位置只返回第一个匹配的位置
  - split方法：以。。。分隔
  - replace方法：用第二个字符串替换第一个

  - 修饰符g   i
    - g表示全局匹配
    - i表示忽略大小写

- 特殊字符

  - .代表除了换行符之外的所有单个字符

    ```javascript
    var reg = /g..gle/gi;
    var str = "googleg--gle";
    console.log(rest.test(str));//true
    console.log(str.match(reg));
    ```

  - *重复多次匹配，匹配任意次（0-n）

    ```javascript
    var reg = /g*gle/gi;
    var str = "ggggle";
    console.log(reg.test(str));//true
    console.log(str.match(reg));
    ```

  - +至少有一次重复匹配

    ```javascript
    var reg = /g+gle/gi;
    var str = "ggle";
    console.log(reg.test(str));
    ```

  - ? 进行0或者1次匹配

    ```javascript
    var reg = /g?gle/gi;
    var str = "ggle";
    console.log(reg.test(str));
    ```

  - []表示可以出现的范围[0-9]

    ```javascript
    var reg = /[a-z]/gi;
    var str = "123m4";
    console.log(reg.test(str));
    ```

  - \w数字字母下划线等同于[0-9||a-z||A-Z||_ ]  \W非数字字母下划线

    ```javascript
    var reg = /\w+/gi;
    var str = "abc13";
    console.log(reg.test(str),str.match(reg));
    ```

  - \d表示数字[0-9]

    ```javascript
    var reg = /\d+/gi;
    var str = "12345abc";
    console.log(reg.test(str),str.match(reg));
    ```

  - \s 匹配空格

    ```javascript
    var reg = /\s+/gi;
    var str = "good good   study";
    console.log(str.replace(reg,""));
    ```

  - {m,n}至少匹配m次，至多匹配n次

    ```javascript
    var reg = /go{3,6}gle/gi;
    var str = "gooogle";
    console.log(reg.test(str));
    ```

  - // /^ 匹配开始$/匹配结尾

    ```javascript
    var reg = /^g.+g$/gi;
    var str = "gooogle";
    console.log(reg.test(str));
    ```

  - |   或

    ```javascript
    var reg = /google|baidu|bing|yahoo/gi;
    var str = "www.baidu.com";
    console.log(reg.test(str));
    ```

    

  - () 分组 将内容作为一个整体进行匹配

    ```javascript
    var reg = /(g.+gle){4,6}/gi;
    var str = "googleaaagooglegooglegooglegoogle";
    console.log(reg.test(str),str.match(reg));
    console.log(RegExp.$1);//获取里面的分组内容
    ```

  - $1 $2分组中的第一个元素和第二个

    ```javascript
    var reg = /(.*)\s(.*)/;
    var str = "taobao baidu";
    
    console.log(str.replace(reg,"$2 $1"));
    ```

### ES6基础语法

#### let的使用

- 用于声明变量。他的用法类似于var，但是声明的变量，只在let命令所在的代码块内有效
- 存在块级作用域{}
- 不存在声明提升
- 不允许重复声明（包括普通变量和函数参数）

#### const的使用

- 用于声明常量，不要试图改变常量的值，其他语法参照let

#### 解构赋值

- 按照一定模式，从数组和对象中提取值，对变量进行赋值

- 数组：

  ```javascript
  let [a,b,c] = [1,2,3];
  ```

- 默认赋值：

  ```javascript
  [a,b=2]=[3];
  let c;
  [a=3]=[c];//不会覆盖2
  ```

- 对象

  ```javascript
  let {a,b}={a:"aaa",b:"bbb"};
  let {a:b}={a:"aaa"};
  let {a,b=5}={a:1};
  ```

#### 模板字符串

- 将变量或表达式直接嵌入字符串

- 使用反引号（``）拼接多行字符串

- ES5

  ```javascript
  var obj = {
      "name": "john",
      age: 18
  };
      var name = obj.name;
      var age = obj.age;
      console.log(name + "的年龄是" + age);
  ```

  ```javascript
  var arr = [0,1,2,3,4];
  let oUl=document.getElementById("test");
  var html="";
  for(var i in arr){
      html+="<li>"+arr[i]+"<li>";
  }
  oUl.innerHTML=html;
  ```

- ES6

  ```javascript
  let obj = {"name":"join","age":20};
  let {name,age}=obj;
  console.log(`${name}的年龄是${age}`);
  ```

  ```javascript
  var arr = [0,1,2,3,4];
  let oUl=document.getElementById("test");
  var html="";
  for(var i in arr){
     	html+=`<li>
  		<a herf="">${arr[i]}</a>
  		
  	<li>`;
  }
  oUl.innerHTML=html;
  ```

#### 箭头函数

- 只含有一个表达式

- 含有多条语句

- this的指向问题

- 没有自己的`this`，`arguments`，`super`或`new.target`。箭头函数表达式更适用于那些本来需要匿名函数的地方，并且它不能用作构造函数。

- 不提供自身的this绑定

- ```javascript
  //ES5
  var foo = function (){
      return 1;
  }
  console.log(foo());
  
  
  //ES6
  let foo = () =>1;
  console.log(foo());
  //传参进去 
  let foo = (a) =>a;
  console.log(foo(10));
  //多条语句
  let foo = (a) =>{
  	let b=10;
      return a+b;
  }
  console.log(foo(10));
  ```

#### this的指向问题

- ES5普通函数的this指针指向window

- 箭头函数不提供自身的 this 绑定（`this` 的值将保持为闭合词法上下文的值）。

- ```javascript
  //ES6
  var foo = () => {
      console.log(this);
  }
  foo(); //this指向window
  ```

- ```javascript
  //ES5写法
         var name = "window";
         var obj = {
             "name": "john",
             "sayHello": function() {
                 console.log(this.name);
             }
         }
         obj.sayHello();
  ```

- ```javascript
  //ES6 this指向定义时所在的作用域而不是执行时的作用域 
          var obj = {
              "name": "john",
              //普通的成员函数
              "sayHello": () => {
                  console.log(this.name);//this指向window
              }
              //定时器版本
              "sayHello":function(){
                  setTimeout(()=>{console.log(this.name)},1000);
              }//john function是在obj里面定义的，所以this指向obj
  			//ES6版本
  			"sayHello":()=>{
                  setTimeout(()=>{console.log(this.name)},1000);//此时指向window
          }
          obj.sayHello();
  //相当于下面的代码		
  		var obj = {};
          obj.name = "john";
          obj.sayHello = () => {huan
              console.log(this.name);
          }
          obj.sayHello();
  ```


#### set结构

- ```javascript
  let set = new Set([1,2,3,4,4]);//构造函数  默认删除相同元素
  
  [...set]//...扩展运算符，将类数组对象转换以逗号分隔的序列
  
  for of//遍历
  console.log(arr);
  for (let i of set) {
      console.log(i); 
  }
  
  set.size//长度
  set.add(0)//加一个元素
  set.delete(0)//删除一个元素
  set.has(0)//判断是否含有一个元素
  set.clear();//清空所有元素
  
  keys()//返回键名的遍历器
  for(let item of set,keys())
  {
      console.log(item);
  }
  
  values() //返回键值的遍历器
  for(let item of set,values())
  {
      console.log(item);
  }
  
  entries() //返回键值对的遍历器
  for(let [key,item] of set,entries())
  {
      console.log(key,item);
  }
  
  forEach()//返回回调函数遍历每个成员
  set.forEach((value,key)=>console.log(value*2))
  /*
  2
  4
  6
  8
  */
  ```


#### map结构

```javascript
let map = new Map([["name","john"],["age",30]]);//设置键值对

map.set(1,1);

map.size//长度

map.set(key,value);//添加键值对
map.get(key);//获取键值对
map.delete(key);
map.has(key);
map.clear();

key();//返回键名的遍历器

values();//返回键值的遍历器

entries();//返回键值对的遍历器

for(let [key,value] ofmap.entries())
    {
        console.log(key,value);
    }

forEach();//使用回调函数遍历每个成员
map.forEach((value,key)=>console.log(value*2))
```

#### 生成器函数（generator）

```javascript
function * foo(x){
    yield x+1;
    yield x+2;
    return x+3;
}
var f = foo(1);
f.next();
console.log(f.next());
//Object{
	done: false//表示该生成集函数是否含有相应的yield或者是否结束
	value: 3
}
//想要继续运行
console.log(f.next(),f.next(),f.next());
```

```javascript
//面试题
//next()里面的参数表示上一级的返回值
function * foo(x){
    var y = 2*(yield(x+1));
    var z = yield(y/3);
    return (x+y+z);
}

var it = foo(5);

console.log(it.next(3));//第一次无论传什么，都是6 即 5+1        value=6
console.log(it.next(12));//yield(x+1)为12，y=24,z=8即24/3	  value=8
console.log(it.next(13));//yield(y/3)为13，z=13			   value=42
```

利用生成器函数编写斐波拉契数列（0	1	1	2	3	5	8	13	21	34...）

```javascript
        function* feibo(n) {
            let a = 0;
            let b = 1;
            for (let i = 0; i < n; i++) {
                yield a;
                let tmp = a + b;
                a = b;
                b = tmp;
            }
            //console.log(tmp);
        }
        var f = feibo(10);
        for (let i of f) {
            console.log(i);
        }

```

#### 类

```javascript
class Person(){
    constructor(name){
        this.name=name;
    }
    sayHello(){
        console.log(this.name);
    }
}
//实例化
var person = new Person("yyvsu");
console.log(person.name);
person.sayHello();
```

### Ajax

#### 简介

- Ajax全称：Asynchronous JavaScript And XML
- 是一种异步加载数据的技术
- 可以通过使用Ajax，实现页面的局部刷新
- 可以不用刷新页面就可以从服务器取得数据，实现局部更新页面

#### 使用

- Ajax的核心对象：XMLHttpRequest
- XHR就是Ajax

##### GET

- 从服务器取得数据

- ```javascript
  <h1></h1>
      <script>
          // 1.创建Ajax对象
          var xhr = new XMLHttpRequest();
          // 2.监听请求
          xhr.onreadystatechange = function() {
                  //当xhr对象的readyState属性发生改变，这个事件就会触发
                  //readyState:
                  // 0 ===>xhr 对象已经创建，但还是没有进行初始化操作
                  // 1 ===>xhr对象已经调用了open
                  // 2 ===>xhr已经发出ajax请求
                  // 3 ===>已经返回了部分数据
                  // 4 ===>数据已经全部返回
                  if (xhr.readyState != 4) {
                      return;
                  }
                  //在200到300之间证明请求是成功的
                  if (xhr.status > 200 & xhr.status <= 300) {
                      //数据放在了xhr.responseText的属性中(string)
                      document.querySelector('h1').innerHTML = xhr.responseText;
                  } else {
                      console.log('请求失败');
                  }
              }
              // 3.打开这个对象
          xhr.open('get', 'test.txt', true);
          // 4.发送请求
          xhr.send();
      </script>
  ```

   

##### POST

- 向服务器传输数据

- ```javascript
  // 1.创建一个xhr对象
          var xhr = new XMLHttpRequest();
          //5.监听数据返回
          xhr.onreadystatechange = function() {
                  if (xhr.readyState != 4) {
                      return;
                  }
                  //在200到300之间证明请求是成功的
                  if (xhr.status >= 200 && xhr.status <= 300) {
                      //数据放在了xhr.responseText的属性中(string)
                      var resp = JSON.parse(xhr.responseText);
                      if (resp.result) {
                          alert('登录成功');
                      } else {
                          alert('运行错误')
                      }
  
                  } else {
                      console.log('请求失败');
                  }
              }
              //2.配置这个对象
          xhr.open('post', './login.php', true);
          //true表示申请的是异步请求
          //3.设定请求头，指明body中的数据是何格式
          xhr.setRequestHeader('Content-Type', 'application/x-www-form-urlencode');
          //发送数据
          xhr.send('user=gap&password=123456');
  ```

  

##### 区别

- GET数据放在url中，大小有限制
- POST放在请求体中，大小无限制，更安全

##### JSON

- JavaScript Object Natation(JS对象简谱)是一种轻量级的数据交换格式
- JSON是ECMA制定的一个数据表示规范
- JS对象的子集，与JS无缝对接
- JSON数据与JS对象的转换
  - JSON->JS:JSON.parse(data)
  - JS->JSON:JSON.stringify(JSObj)

##### 回调地狱

- ```javascript
  //获取数据 
          //要使这三个函数成功前提是假设三个函数都是同步的
          x = getData();
          y = getMoreData(x);
          z = getMoreData(y);
  
  
          // 若三个函数是异步的
          //x,y后面的函数就是回调函数
          // 前一次的结果最后后i一次的输入
          getData(function(x) {
              getMoreData(x, function(y) {
                  getMoreData(y, function(z) {
                      //process z,
                  })
              })
          })
  ```

- 一层层嵌套，这样会导致回调层级很深，导致开发和维护都很难，在ES6中提出了promise这样的对象来解决回调地狱的问题

##### promise

- ```javascript
  //通过Promise这个构造函数来创建一个对象
  //这个promise对象，有三种状态：padding(准备状态)，fulfill(promise返回满足条件的状态),reject(延时对象没有满足)
  //promise构造函数，有一个参数，这个参数是一个回调函数。这个回调，接收两个参数，这两个参数，都能够改变promise对象的状态
  //第一个参数可以将状态从pending===>fulfill,而第二个参数，可以将状态从pending===>reject
  //fulfill表示调用成功，reject表示调用失败
  // var promise = new Promise(function(resolve, reject) {//回调参数
  //     if ( /*成功*/ ) {
  //         resolve()
  //     } else {
  //         reject();
  //     }
  // })
  ```

- Ajax对调用顺序是有依赖性的

- ```javascript
  <script src="jquery-3.2.1.min.js"></script>
      <script>
          var article = ' ';
          $.get('./p1.txt', function(p1) {
              article += p1 + '<br>';
              $.get('./p2.txt', function(p2) {
                  article += p2 + '<br>';
                  $.get('./p3.txt', function(p3) {
                      article += p3 + '<br>';
                      $.get('./p4.txt', function(p4) {
                          article += p4 + '<br>';
                          $('p').html(article);
                      })
                  })
              })
          })
      </script>
  ```

  

