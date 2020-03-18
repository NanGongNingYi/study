如果**在body中使用脚本，则应把脚本置于 \<body> 元素的底部**，可改善显示速度，因为脚本编译会拖慢显示

如果使用js文件，则应该在head中这样引用  
```javascript
<script src="myScript.js"><script>
```
如需向一张页面添加多个脚本文件 - 请使用多个 script 标签
**每行js代码需要用";"作为结束符**

|关键词|描述|
|------|------|
|var|声明变量|
|function|声明函数|
|return|退出函数|
|if else|标记需被执行的语句块，根据某个条件|
|switch|标记需被执行的语句块，根据不同的情况|
|do while|执行语句块，并在条件为真时重复代码块|
|for|标记需被执行的语句块，只要条件为真|
|break|终止 switch 或循环|
|continue|跳出循环并在顶端开始|
|try catch|对语句块实现错误处理|
|debugger|停止执行 JavaScript，并调用调试函数（如果可用）|
|typeof|返回变量的类型|
|instanceof|返回 true，如果对象是对象类型的实例|

**JavaScript 对大小写敏感**

在脚本的开头声明所有变量是个好习惯！

javascript支持一个语句，多个变量
```javascript
 var person = "Bill Gates", carName = "porsche", price = 15000;
```
**undefined&&null**
未提供值的变量，它的值将是undefined
任何变量均可通过设置值为 undefined 进行清空。其类型也将是 undefined

在 JavaScript 中，null 的数据类型是对象
可以通过设置对象值为 null 来清空对象；也可以通过设置值为 undefined 清空对象

Undefined 与 null 的值相等，但类型不相等

如果对数字和字符串相加，结果将是字符串

**\*\*是幂运算**

JavaScript 从左向右计算表达式，不同的次序会产生不同的结果。

JavaScript 变量能够保存多种数据类型：数值、字符串值、数组、对象等等：
```javascript
var length = 7; // 数字
var lastName = "Gates"; // 字符串
var cars = ["Porsche", "Volvo", "BMW"]; // 数组
var x = {firstName:"Bill", lastName:"Gates"}; //JavaScript 对象用花括号来书写
```
JavaScript 拥有动态类型。这意味着相同变量可用作不同类型：
```javascript
var x;               // 现在 x 是 undefined
var x = 7;           // 现在 x 是数值
var x = "Bill";      // 现在 x 是字符串值
```
javascript字符串可以用单引号也可以用双引号包围

JavaScript 只有一种数值类型,写数值时用不用小数点均可。超大或超小的数值可以用科学计数法来写。
```javascript
var y = 123e5;      // 12300000
var z = 123e-5;     // 0.00123
```
布尔值只有两个值：true 或 false。
```javascript
var x = true;
var y = false;
```
**javascript"\=="和"\==="的区别**
console(34 == "34")  输出true
console(34 === "34")  输出false
==  只判断值，不判断类型，实际上里面有类型转换
=== 不仅判断值，还需要判断类型，只有两者都相同时，才会输出true

**typeof**
typeof 运算符可返回以下原始数据类型之一：
string
number
boolean
undefined

typeof 运算符可返回以下复杂数据类型之一：
function //返回函数
object //返回对象
```javascript
typeof {name:'Bill', age:62} // 返回 "object"
typeof [1,2,3,4]             // 返回 "object" (并非 "array"，因为在 JavaScript 中数组即对象)
typeof function myFunc(){}   // 返回 "function"
```

#函数

    function 函数名(参数 1, 参数 2, 参数 3) {
    要执行的代码;
    }
##函数调用
- 当事件发生时（当用户点击按钮时）
- 当 JavaScript 代码调用时
- 自动的（自调用）

##函数返回
当 JavaScript 到达 return 语句，函数将停止执行并返回值

#对象
##属性
```javascript
var person = { //属性没写完之前都是用','分割的
  firstName: "Bill",
  lastName : "Gates",
  id       : 678,
  fullName : function() { //方法也可以作为对象的属性
    return this.firstName + " " + this.lastName;
  }
}; //注意最后有个分号
```
##访问对象属性
1. objectName.propertyName
2. objectName["propertyName"]

例如：```
person.lastName\
person["lastName"];```
##访问函数方法
<font color="red">？这句话啥意思</font>
如果不使用 () 访问 fullName 方法，则将返回函数定义
##创建对象
通过关键词 "new" 来声明 JavaScript 变量，则该变量会被创建为对象：
不要把字符串、数值和布尔值声明为对象，会增加代码的复杂性并降低执行速度。

#HTML事件
HTML 事件是发生在 HTML 元素上的“事情”
|事件|描述|
|---|---|
|onchange|	HTML 元素已被改变|
|onclick	|用户点击了 HTML 元素|
|onmouseover	|用户把鼠标移动到 HTML 元素上|
|onmouseout	|用户把鼠标移开 HTML 元素|
|onkeydown	|用户按下键盘按键|
|onload	|浏览器已经完成页面加载|
##事件处理程序
事件处理程序可用于处理、验证用户输入、用户动作和浏览器动作：
- 每当页面加载时应该做的事情
- 当页面被关闭时应该做的事情
- 当用户点击按钮时应该被执行的动作
- 当用户输入数据时应该被验证的内容
- 等等

JavaScript 处理事件的不同方法有很多：
- HTML 事件属性可执行 JavaScript 代码
- HTML 事件属性能够调用 JavaScript 函数
- 能够向 HTML 元素分配自己的事件处理函数
- 能够阻止事件被发送或被处理
- 等等

#长代码换行
某条 JavaScript 语句不适合一整行，那么最佳换行位置是某个运算符之后

    document.getElementById("demo")innerHTML =
    "Hello Kitty.";

也可以在字符串中换行：对长字符串换行的最安全做法（但是有点慢）是使用字符串加法

    document.getElementById("demo").    innerHTML = "Hello" + 
    "Kitty!";

|字符串方法|描述|
|---|---|
|indexOf() |返回字符串中指定文本首次出现的索引（位置），找不到则返回-1|
|lastIndexOf() |返回指定文本在字符串中最后一次出现的索引，找不到则返回-1|
|search() |搜索特定值的字符串，并返回匹配的位置|
|slice() |提取字符串的某个部分并在新字符串中返回被提取的部分|
|substring() |类似于 slice()不同之处在于 substring() 无法接受负的索引|
|substr()|类似于slice()不同之处在于第二个参数规定被提取部分的长度|
|replace()|用另一个值替换在字符串中指定的值|
|toUpperCase() |把字符串转换为大写|
|toLowerCase() |把字符串转换为小写|
|concat() |连接两个或多个字符串,可用于代替加运算符|
|trim() |方法删除字符串两端的空白符;Internet Explorer 8 或更低版本不支持|
|charAt() |方法返回字符串中指定下标（位置）的字符串|
|charCodeAt()|方法返回字符串中指定索引的字符 unicode 编码|
|使用[]访问字符串内部|如果找不到字符，[ ] 返回 undefined，而 charAt() 返回空字符串；它是只读的|
|split() |将字符串转换为数组|

#数字
JavaScript 不会定义不同类型的数，比如整数、长的、浮点等等；JavaScript 数值始终以双精度浮点数来存储

NaN 属于 JavaScript 保留词，指示某个数不是合法数
NaN 是数，typeof NaN 返回 number
isNaN() 判断某个值是否是数

Infinity （或 -Infinity）是 JavaScript 在计算数时超出最大可能数范围时返回的值
Infinity 是数：typeOf Infinity 返回 number

avaScript 会把前缀为 0x 的数值常量解释为十六进制

绝不要用前导零写数字（比如 07），一些 JavaScript 版本会把带有前导零的数解释为八进制

toString() 方法把数输出为十六进制、八进制或二进制

    var myNumber = 128;
    myNumber.toString(16);     // 返回 80
    myNumber.toString(8);      // 返回 200
    myNumber.toString(2);      // 返回 10000000

##数值属性
|属性|	描述|
|---|---|
|MAX_VALUE	|返回 JavaScript 中可能的最大数|
|MIN_VALUE	|返回 JavaScript 中可能的最小数|
|NEGATIVE_INFINITY	|表示负的无穷大（溢出返回）|
|NaN	|表示非数字值（"Not-a-Number"）|
|POSITIVE_INFINITY	|表示无穷大（溢出返回）|

数值属性属于名为 number 的 JavaScript 数字对象包装器；这些属性只能作为 Number.MAX_VALUE 访问

#正则表达式
用正则表达式执行搜索字符串中 "w3school" 的大小写不敏感的搜索：

    var str = "Visit W3School";
    var n = str.search(/w3school/i); 

##正则表达式修饰符
|修饰符|	描述|
|---|---|
|i	|执行对大小写不敏感的匹配|
|g	|执行全局匹配(查找所有匹配而非在找到第一个匹配后停止)|
|m	|执行多行匹配|
||更多内容请查看js手册|

#异常

    try {
         供测试的代码块
    }
     catch(err) {
         处理错误的代码块
    } 
JavaScript 将抛出异常（抛出错误），会创建带有两个属性的 Error 对象：name 和 message

    throw 语句允许您创建自定义错误

    try {
         供测试的代码块
    }
     catch(err) {
         处理错误的代码块
    } 
    finally {
         无论 try / catch 结果如何都执行的代    码块
    }

#作用域
在函数中声明的变量，会成为函数的局部变量
函数参数也是函数内的局部变量
函数之外声明的变量，会成为全局变量，网页的所有脚本和函数都能够访问它
如果为给未声明的变量赋值，此变量会自动成为全局变量。

    myFunction();

    // 此处的代码能够使用 carName 变量

    function myFunction() {
        carName = "porsche";
    }

在 HTML 中，全局作用域是 window，所有全局变量均属于 window 对象
除非有意为之，否则请勿创建全局变量

局部变量会在函数完成时被删除
全局变量会在您关闭页面是被删除

#Hoisting 
Hoisting 是 JavaScript 将所有声明提升到当前作用域顶部的默认行为（提升到当前脚本或当前函数的顶部），即可以在声明变量之前使用变量

    x = 5; // 把 5 赋值给 x
    elem = document.getElementById("demo"); //  查找元素
    elem.innerHTML = x;  // 在元素中显示 x
    var x; // 声明 x

只有声明（var y）而不是初始化（=7）被提升到顶部。y 在其被使用前已经被声明，但是由于未对初始化进行提升，y 的值仍是未定义

    var x = 5; // 初始化 x
    elem = document.getElementById("demo"); //  查找元素
    elem.innerHTML = x + " " + y;// 显示 x 和 y
    var y = 7; // 初始化 y 

#use strict
"use strict"; 的作用是指示 JavaScript 代码应该以“严格模式”执行
通过在脚本或函数的**开头**添加 "use strict"; 来声明严格模式。
在脚本开头进行声明，拥有全局作用域（脚本中的所有代码均以严格模式来执行）

#let 和 const
let 和 const 提供了块作用域（Block Scope）变量（和常量）
const 定义的变量与 let 变量类似，但不能重新赋值
const 变量必须在声明时赋值

请使用 {} 来代替 new Object()
请使用 "" 来代替 new String()
请使用 0 来代替 new Number()
请使用 false 来代替 new Boolean()
请使用 [] 来代替 new Array()
请使用 /()/ 来代替 new RegExp()
请使用 function (){}来代替 new Function()

请使用 default 来结束您的 switch 语句。即使您认为没有这个必要

#JSON
JSON 是存储和传输数据的格式
JSON 经常在数据从服务器发送到网页时使用
JSON 格式在语法上与创建 JavaScript 对象的代码相同,所以JavaScript 程序可以很容易地将 JSON 数据转换成本地的 JavaScript 对象

##JSON语法规则
数据是名称/值对："firstName":"Bill"
数据由逗号分隔
花括号保存对象：对象能够包含多个名称/值对
{"firstName":"Bill", "lastName":"Gates"} 
方括号保存数组：数组能够包含对象
"employees":[
    {"firstName":"Bill", "lastName":"Gates"}, 
    {"firstName":"Steve", "lastName":"Jobs"}, 
    {"firstName":"Alan", "lastName":"Turing"}
]
##把 JSON 文本转换为 JavaScript 对象
JSON 的通常用法是从 web 服务器读取数据，然后在网页中显示数据
首先，创建包含 JSON 语法的 JavaScript 字符串

    var text = '{ "employees" : [' +
    '{ "firstName":"Bill" , "lastName":"Gates" },   ' +
    '{ "firstName":"Steve" , "lastName":"Jobs" },   ' +
    '{ "firstName":"Alan" , "lastName":"Turing" }   ]}';
然后，使用 JavaScript 的内建函数 JSON.parse() 来把这个字符串转换为 JavaScript 对象

    var obj = JSON.parse(text);
最后，在页面中使用这个新的 JavaScript 对象

    <p id="demo"></p>
    <script>
    document.getElementById("demo").innerHTML =
    obj.employees[1].firstName + " " + obj. employees[1].lastName;
    </script> 

数据验证
服务器端验证是由 web 服务器执行的，在输入被送往服务器之后
客户端验证是由 web 浏览器执行的，在输入被送往 web 服务器之前

#对象
在 JavaScript 中，几乎“所有事物”都是对象。
布尔是对象（如果用 new 关键词定义）
数字是对象（如果用 new 关键词定义）
字符串是对象（如果用 new 关键词定义）
日期永远都是对象
算术永远都是对象
正则表达式永远都是对象
数组永远都是对象
函数永远都是对象
对象永远都是对象
所有 JavaScript 值，除了原始值，都是对象
原始值指的是没有属性或方法的值。

原始数据类型指的是拥有原始值的数据。
JavaScript 定义了 5 种原始数据类型：
- string
- number
- boolean
- null
- undefined

for...in 语句遍历对象的属性

    for (variable in object) {
        要执行的代码
    }
for...in 循环中的代码块会为每个属性执行一次

delete 关键词从对象中删除属性：

    var person = {firstName:"Bill",     lastName:"Gates", age:62,   eyeColor:"blue"};
    delete person.age;   // 或 delete person    ["age"];

|属性|	值|
|---|---|
|firstName|	Bill|
|lastName|	Gates|
|age|	62|
|eyeColor|	blue|
|fullName|	function() {return this.|firstName + " " + this.lastName;}|

##构造函数
    function Person(first, last, age,   eyecolor) {
        this.firstName = first;
        this.lastName = last;
        this.age = age;
        this.eyeColor = eyecolor;
        this.nationality = "English";
    }

#函数
    var myFunction = function (a, b)    {return a * b};
    var x = myFunction(4, 3);

##自调用函数
不需要其他变量来调用，定义完了就可以在运行时自己调用

    (function () {
        var x = "Hello!!";  //我会调用我    自己
    })();
JavaScript 函数都有属性和方法。
arguments.length 会返回函数被调用时收到的参数数目
toString() 方法以字符串返回函数
##箭头函数
箭头函数没有自己的 this。它们不适合定义对象方法。
箭头函数未被提升。它们必须在使用前进行定义
使用 const 比使用 var 更安全，因为函数表达式始终是常量值

    const x = (x, y) => { return x * y };
##函数参数
函数定义不会为参数规定数据类型。
函数不会对所传递的参数实行类型检查。
函数不会检查所接收参数的数量

    functionName(parameter1, parameter2,    parameter3) {
        要执行的代码
    }

##call方法
通过 call()，您能够使用属于另一个对象的方法
本例调用 person 的 fullName 方法，并用于 person1

    var person = {
        fullName: function() {
            return this.firstName + " " +   this.lastName;
        }
    }
    var person1 = {
        firstName:"Bill",
        lastName: "Gates",
    }
    person.fullName.call(person1);  // 将返回 "Bill Gates"

call() 方法可接受参数

    var person = {
      fullName: function(city, country) {
        return this.firstName + " " + this. lastName + "," + city + "," +    country;
      }
    }
    var person1 = {
      firstName:"Bill",
      lastName: "Gates"
    }
    person.fullName.call(person1, "Seattle", "USA");

##apply方法
apply() 方法，能够编写用于不同对象的方法

    var person = {
        fullName: function() {
            return this.firstName + " " +   this.lastName;
        }
    }
    var person1 = {
        firstName: "Bill",
        lastName: "Gates",
    }
    person.fullName.apply(person1);  // 将返回 "Bill Gates"
###call与apply
call() 方法分别接受参数
apply() 方法接受数组形式的参数

不通过关键词 var 创建的变量总是全局的，即使它们在函数中创建
拥有相同名称的全局变量和局部变量是不同的变量。修改一个，不会改变其他

#HTML DOM 
HTML DOM 是关于如何获取、更改、添加或删除 HTML 元素的标准

HTML DOM 方法：能够（在 HTML 元素上）执行的动作
HTML DOM 属性：能够设置或改变的 HTML 元素的值
在 DOM 中，所有 HTML 元素都被定义为对象

    <html>
    <body>
    <p id="demo"></p>
    <script>
    document.getElementById("demo").innerHTML = "Hello World!";
    </script>
    </body>
    </html>
getElementById 是方法，innerHTML 是属性

取元素内容最简单的方法是使用 innerHTML 属性
innerHTML 属性可用于获取或改变任何 HTML 元素，包括 \<html> 和 \<body>

document.getElementById(id).onclick = function(){code}	向 onclick 事件添加事件处理程序

##查找HTML元素方法
- 通过 id 查找 HTML 元素
- 通过标签名查找 HTML 元素
- 通过类名查找 HTML 元素
- 通过 CSS 选择器查找 HTML 元素
- 通过 HTML 对象集合查找 HTML 元素
查找 "main" 中所有 <p> 元素
    var x = document.getElementById("main");
    var y = x.getElementsByTagName("p"); 
查找匹配指定 CSS 选择器（id、类名、类型、属性、属性值等等）的所有 HTML 元素
    var x = document.querySelectorAll("p.intro");

document.write() 可用于直接写入 HTML 输出流;不要在文档加载后使用 document.write()，会覆盖文档
修改 \<img> 元素的 src 属性的值

    <img id="myImage" src="smiley.gif">
    <script>
    document.getElementById("myImage").src = "landscape.jpg";
    </script>
##css

    <p id="p2">Hello World!</p>
    <script>
    document.getElementById("p2").style.color = "blue";
    </script>

##动画

    function myMove() {
        var elem =  document.getElementById("animate"); 
        var pos = 0;
        var id = setInterval(frame, 5);//每5秒执行一次
         function frame() {
            if (pos ==  350) {
                 clearInterval(id);//停止setInterval
            } else {
                 pos++; 
                 elem.style.top = pos + 'px'; 
                 elem.style.left = pos + 'px'; 
            }
         }
    }


    <p>请点击“试一试”按钮，以执行 displayDate() 函数。</p>
    <button id="myBtn">试一试</button>
    <p id="demo"></p>
    <script>//这里displayDate为什么加了括号就直接显示时间了？
    document.getElementById("myBtn").onclick = displayDate;
    function displayDate() {
      document.getElementById("demo").innerHTML = Date();
    }
    </script>

###事件监听器
    element.addEventListener(event, function, useCapture);
第一个参数是事件的类型（比如 "click" 或 "mousedown"）
第二个参数是当事件发生时我们需要调用的函数
第三个参数是布尔值，指定使用事件冒泡还是事件捕获，此参数是可选的

向相同元素添加多个事件处理程序
addEventListener() 方法允许您向相同元素添加多个事件，同时不覆盖已有事件
可以将事件监听器添加到任何 HTML DOM 对象上，比如 HTML 元素、HTML 对象、window 对象或其他支持事件的对象，比如 xmlHttpRequest 对象

在 HTML DOM 中有两种事件传播的方法：冒泡和捕获。

事件传播是一种定义当发生事件时元素次序的方法。假如 \<div> 元素内有一个 \<p>，然后用户点击了这个 \<p> 元素，应该首先处理哪个元素“click”事件？
在冒泡中，最内侧元素的事件会首先被处理，然后是更外侧的：首先处理 \<p> 元素的点击事件，然后是 \<div> 元素的点击事件
在捕获中，最外侧元素的事件会首先被处理，然后是更内侧的：首先处理 \<div> 元素的点击事件，然后是 \<p> 元素的点击事件

在 addEventListener() 方法中，通过使用“useCapture”参数来规定传播类型:
addEventListener(event, function, useCapture)
默认值是 false，将使用冒泡传播，如果该值设置为 true，则事件使用捕获传播

removeEventListener() 方法会删除已通过 addEventListener() 方法附加的事件处理程序

##节点

    <title id="demo">DOM 教程</title> 
（上面例子中的）元素节点 \<title> 不包含文本
它包含了值为 "DOM 教程" 的文本节点
文本节点的值能够通过节点的 innerHTML 属性进行访问
访问 innerHTML 属性等同于访问首个子节点的 nodeValue

    var myTitle = document.getElementById("demo").firstChild.nodeValue;
innerHTML 可以取回 HTML 元素的内容

###nodeName 属性规定节点的名称
nodeName 是只读的
元素节点的 nodeName 等同于标签名
属性节点的 nodeName 是属性名称
文本节点的 nodeName 总是 #text
文档节点的 nodeName 总是 #document
nodeName 总是包含 HTML 元素的大写标签名

nodeValue 属性规定节点的值
元素节点的 nodeValue 是 undefined
文本节点的 nodeValue 是 文本文本
属性节点的 nodeValue 是 属性值

###创建节点
这段代码创建了一个新的\ <p> 元素：
var para = document.createElement("p");
如需向 \<p> 元素添加文本，则必须首先创建文本节点。这段代码创建了一个文本节点：
var node = document.createTextNode("这是一个新段落");
然后您需要向 \<p> 元素追加这个文本节点：
para.appendChild(node);
最后您需要向已有元素追加这个新元素
这段代码查找一个已有的元素：
var element = document.getElementById("div1");
这段代码向这个已有的元素追加新元素：
element.appendChild(para);

appendChild() 方法，追加新元素作为父的最后一个子

找到你想要删除的子，并利用其 parentNode 属性找到父
var child = document.getElementById("p1");
child.parentNode.removeChild(child);

HTMLCollection 是 HTML 元素的集合
NodeList 是文档节点的集合
NodeList 和 HTML 集合几乎完全相同
HTMLCollection 和 NodeList 对象都是类数组的对象列表（集合）
访问 HTMLCollection 项目，可以通过它们的名称、id 或索引号
访问 NodeList 项目，只能通过它们的索引号