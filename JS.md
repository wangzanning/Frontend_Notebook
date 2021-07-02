- [Javascript操作DOM常用API总结](https://www.cnblogs.com/lrzw32/p/5008913.html#_label1)

  ```javascript
  var div = document.createElement("div");
  var textNode = document.createTextNode("一个TextNode");
  parent.appendChild(child);
  parentNode.insertBefore(newNode,refNode);
  var deletedChild = parent.removeChild(node);
  element.setAttribute(name, value);
  var value = element.getAttribute("id");
  ```

- [学习Javascript闭包（Closure）](http://www.ruanyifeng.com/blog/2009/08/learning_javascript_closures.html)

  闭包允许从内部函数访问外部函数的作用域。

  最大用处有两个：一个是可以读取父函数内部的变量，另一个就是让这些变量的值始终保持在内存中。

- [回味JS基础:call apply 与 bind](https://juejin.cn/post/6844903444348665870)***[ ! important ]***

- [关于call、apply和bind](https://www.cnblogs.com/fengyuexuan/p/12408624.html)***[ ! important ]***

  func.call, 使用一个指定的方法，和若干个参数，调用某个函数

  func.apply, 类似call，第二个参数是数组

  bind 创建一个新函数，不执行，返还一个新函数的引用，多用于继承

- [深入理解Js回调函数](https://www.cnblogs.com/xiaonian8/p/14113547.html)

  函数作为参数传递给另一个函数，外部函数内部调用这个回调函数，完成某种操作。

  使用promise，async/await 避免回调地域

- [null、NaN和undefined的区别总结](https://blog.csdn.net/master_yao/article/details/78903889)

- [undefined，not defined,null和NaN的区别](https://blog.csdn.net/weixin_28900307/article/details/88079057?utm_medium=distribute.pc_relevant.none-task-blog-BlogCommendFromMachineLearnPai2-2.control&dist_request_id=370feb85-1268-4cc4-8c41-0e2c38bbc815&depth_1-utm_source=distribute.pc_relevant.none-task-blog-BlogCommendFromMachineLearnPai2-2.control)

  1）undefined与null是相等；（2）NaN与任何值都不相等，与自己也不相等

  `null`表示一个变量`已声明定义了一个空值`，表示一个**空对象**，是一个**关键字**

  `NaN`是一种数字类型，常用作数字运算返回的结果中，表示结果`无法转化成数字的数字类型`，它不等于自身

  type of分别是undefined，object，number

- [JavaScript 中对象的深拷贝](https://www.sohu.com/a/117842628_505800)

- [js中的map(parseInt)](https://blog.csdn.net/The_X_One/article/details/83584019?utm_medium=distribute.pc_relevant.none-task-blog-BlogCommendFromMachineLearnPai2-3.control&dist_request_id=f660fb39-8ce9-46d2-b573-fa218cbc4cc4&depth_1-utm_source=distribute.pc_relevant.none-task-blog-BlogCommendFromMachineLearnPai2-3.control)

  ```javascript
  'use strict';
  
  var arr = ['1', '2', '3'];
  var r;
  
  r = arr.map(parseInt);
  console.log(r);
  //1, NaN, NaN
  ```

  

- [async/await执行原理详解 - 简书](https://www.jianshu.com/p/72e36168944f)

  await语句后面的代码，相当于回调函数。（即：await的下一行开始，都视作回调函数的内容）

  回调函数会被压入microtask队列，当主线程调用栈被清空时，去microtask队列里取出各个回调函数，逐个执行。

- [原始类型和对象类型的区别](https://www.cnblogs.com/nayek/p/11671118.html)

  **基本数据类型**：**Number、String、Boolean、Null、 Undefined、Symbol（ES6），**这些类型可以直接操作保存在变量中的实际值。

  **引用数据类型**：**Object（在JS中除了基本数据类型以外的都是对象，数据是对象，函数是对象，正则表达式是对象）**

- [变量声明提升](https://blog.csdn.net/qq673318522/article/details/50810650?utm_medium=distribute.pc_relevant.none-task-blog-BlogCommendFromMachineLearnPai2-1.control&dist_request_id=08f9d12c-23fe-4262-b865-03b2a2995186&depth_1-utm_source=distribute.pc_relevant.none-task-blog-BlogCommendFromMachineLearnPai2-1.control)***[ ! important ]***

  变量和函数在声明之前已经可用，即JavaScript函数里的所有声明（只是声明，但不涉及赋值）都被提前到函数体的顶部

  函数声明提升优于变量声明提升，但变量赋值依然保留在原来的位置

- [javascript中的伪数组](https://www.pianshen.com/article/1706294856/)

  1. 具有`length`属性；按索引方式存储数组；不具有数组的方法

  2. ```
     伪数组转真数组
     Array.prototype.slice.call(liArr.children) 
     ```

- [箭头函数与普通函数的区别](https://www.cnblogs.com/biubiuxixiya/p/8610594.html)***[ ! important ]***

  箭头函数：匿名函数，不能作为构造函数，不能使用new，箭头函数不绑定this，会捕获其所在的上下文的this值，作为自己的this值； 箭头函数通过 call() 或  apply() 方法调用一个函数时，只传入了一个参数，对 this 并没有影响。箭头函数没有原型属性

  ```javascript
  var obj = {
    a: 10,
    b: () => {
      console.log(this.a); // undefined
      console.log(this); // Window {postMessage: ƒ, blur: ƒ, focus: ƒ, close: ƒ, frames: Window, …}
    },
    c: function() {
      console.log(this.a); // 10
      console.log(this); // {a: 10, b: ƒ, c: ƒ}
    }
  }
  obj.b(); 
  obj.c();
  
  var obj = {
    a: 10,
    b: function(){
      console.log(this.a); //10
    },
    c: function() {
       return ()=>{
             console.log(this.a); //10
       }
    }
  }
  obj.b(); 
  obj.c()();
  ```

- [forEach参数详解，forEach与for循环区别](https://www.cnblogs.com/echolun/p/11544045.html)

  forEach不支持break，forEach中使用return无效； forEach删除自身元素index不会被重置

  for循环过程中支持修改索引（修改 i），但forEach做不到（底层控制index自增，我们无法左右它）

- [JS之Generator生成器](https://blog.csdn.net/lu1024188315/article/details/73322640)

- ```javascript
  function* gen(x){
    var y = yield x + 2;
    return y;
  }
  ```

  next 方法的作用是分阶段执行 Generator 函数。每次调用 next 方法，会返回一个对象，这个对象就是具有两个属性（done (done=false) 和 value (value=operand)）的 IteratorResult 对象

- [js 原型链](https://www.jianshu.com/p/08c07a953fa0)

- [JS原型、原型链深入理解](https://www.jb51.net/article/80109.htm)***[ ! important ]***

  原型链：每个对象都可以有一个原型\_\_proto\_\_，这个原型还可以有它自己的原型，以此类推，形成一个原型链

  prototype属性，它是**函数所独有的**，它是从**一个函数指向一个对象**。它的含义是**函数的原型对象**，这个对象的用途就是包含所有实例共享的属性和方法。当一个函数被用作构造函数来创建实例时，该函数的prototype属性值将被作为原型赋值给所有对象实例（也就是设置实例的\_\_proto\_\_属性）

  \_\_proto\_\_ 是原型链查询中实际用到的，它总是指向 prototype，换句话说就是指向构造函数的原型对象，它是**对象独有的。**

  所有的原型对象都有constructor属性，constructor属性是创建实例对象的函数的引用，我们可以使用该属性创建新的对象。

- [js继承的6种方式](https://www.cnblogs.com/ranyonsue/p/11201730.html)***[ ! important ]***

  （1）原型链继承：让新实例的原型等于父类的实例。

  特点：实例可继承的属性有：实例的构造函数的属性，父类构造函数属性，父类原型的属性。（新实例不会继承父类实例的属性！）
  缺点：1、新实例无法向父类构造函数传参。
  　　　2、继承单一。
  　　　3、所有新实例都会共享父类实例的属性。（原型上的属性是共享的，一个实例修改了原型属性，另一个实    			例的原型属性也会被修改！）

  ```javascript
  son.prototype = new Father();
  ```

  （2）借用构造函数继承：用.call()和.apply()将父类构造函数引入子类函数。

  ```javascript
  Person.call(this, "func");
  ```

  　特点：1、只继承了父类构造函数的属性，没有继承父类原型的属性。
  　　　　2、解决了原型链继承缺点1、2、3。
  　　　　3、可以继承多个构造函数属性（call多个）。
  　　　　4、在子实例中可向父实例传参。
  　缺点：1、只能继承父类构造函数的属性。
      　　　2、无法实现构造函数的复用。（每次用每次都要重新调用）
  　　　　3、每个新实例都有父类构造函数的副本，臃肿。

- [JS判断数组的六种方法详解](https://segmentfault.com/a/1190000017790888)

- [js判断类型](https://segmentfault.com/a/1190000018740340?utm_source=sf-related)***[ ! important ]***

  判断数组：

  ```javascript
  let arr = [];
  //instanceof 主要是用来判断某个实例是否属于某个对象
  console.log(arr instanceof Array); // true
  //对象构造函数的 constructor判断
  console.log(arr.constructor === Array); // true
  //Object.prototype.toString
  console.log(Object.prototype.toString.call(arr) === '[object Array]'); // true
  //Array.isArray ES5新增
  console.log(Array.isArray(arr)); // true
  ```

  判断对象

  ```javascript
  let obj = {};
  // 1.Object.prototype.toString
  console.log(Object.prototype.toString.call(obj) === '[Object Object]'); 
  // 2.constructor
  console.log(obj.constructor === Object);
  // 3.$.type() 
  console.log($.type(obj) === 'object');
  ```

  判断对象是否为空

  ```javascript
  let obj = {}
  // 1.JSON
  console.log(JSON.stringify(obj) === '{}');
  //es6 利用Object.keys()
  console.log(Object.keys(obj).length === 0);
  
  ```

  判断数组是否为空

  ```javascript
  let arr = [];
  (arr && arr.length > 0) ? console.log('不为空数组！') : console.log('空数组！');
  console.log(Array.isArray(arr) && arr.length === 0);
  ```

  五大常见方法：

  ```
  //tyepof 操作符返回一个字符串，表示未经计算的操作数的类型，用于除null、对象和数组之外的通用类型的判断方法
  //Object.prototype.toString.call() 原生原型扩展函数，用来精确的区分数据类型，万能
  //$.type() 用于确定JavaScript内置对象的类型，并返回小写形式的类型名称，万能
  //instanceof 该运算符用于测试构造函数的prototype属性是否出现在对象的原型链中的任何位置，用于检测引用类型的判断方法，针对Array和RegExp进行判断。
  //constructor 该属性返回对创建此对象的数组函数的引用，每个具有原型的对象都会自动获得constructor属性
  ```

- [函数作用域](https://blog.csdn.net/weixin_40387601/article/details/80515665)

- [for in 和for of的区别 - 简书](https://www.jianshu.com/p/c43f418d6bf0)

  for in更适合遍历对象，不要使用for in遍历数组，会可能不按照实际数组内部顺序遍历

  for in 可以遍历到myObject的原型方法method,如果不想遍历原型方法和属性的话，可以在循环内部判断一下,hasOwnPropery 方法可以判断某属性是否是该对象的实例属性

  ```javascript
  for (var key in myObject) {
  　　if（myObject.hasOwnProperty(key)){
  　　　　console.log(key);
  　　}
  }
  ```

- [this的4种绑定规则](https://www.cnblogs.com/xiaohuochai/p/5735901.html)***[ ! important ]***

  **默认绑定：**全局环境中，this默认绑定到window，函数独立调用时，this默认绑定到window，被嵌套的函数独立调用时，this默认绑定到window

  **隐式绑定：**被直接对象所包含的函数调用时，也称为方法调用，this隐式绑定到该直接对象

  **隐式丢失：**隐式丢失是指被隐式绑定的函数丢失绑定对象，从而默认绑定到window。这种情况容易出错却又常见

  ```javascript
  var a = 0;
  function foo(){
      console.log(this.a);
  };
  var obj = {
      a : 2,
      foo:foo
  }
  //把obj.foo赋予别名bar，造成了隐式丢失，因为只是把foo()函数赋给了bar，而bar与obj对象则毫无关系
  var bar = obj.foo;
  bar();//0
  ```

  **显示绑定：**通过call()、apply()、bind()方法把对象绑定到this上，叫做显式绑定。对于被调用的函数来说，叫做间接调用

  **new绑定：**如果函数或者方法调用之前带有关键字new，它就构成构造函数调用。

  ```javascript
  //如果构造函数使用return语句但没有指定返回值，或者返回一个原始值，那么这时将忽略返回值，同时使用这个新对象作为调用结果
  function fn(){
      this.a = 2;
      return;
  }
  var test = new fn();
  console.log(test);//{a:2}
  //如果构造函数显式地使用return语句返回一个对象，那么调用表达式的值就是这个对象
  var obj = {a:1};
  function fn(){
      this.a = 2;
      return obj;
  }
  var test = new fn();
  console.log(test);//{a:1}
  ```

  严格模式下，独立调用的函数的this指向undefined，

- [深入理解this机制箭头函数](https://www.cnblogs.com/xiaohuochai/p/5737876.html)***[ ! important ]***

  箭头函数根据当前的[词法作用域](http://www.cnblogs.com/xiaohuochai/p/5700095.html)而不是根据[this机制顺序](http://www.cnblogs.com/xiaohuochai/p/5737435.html)来决定this，所以，箭头函数会继承外层函数调用的this绑定，而无论this绑定到什么

  注意事项：this在箭头函数中被绑定，4种[绑定规则](http://www.cnblogs.com/xiaohuochai/p/5735901.html)中的无论哪种都无法改变其绑定；不可以当作构造函数，也就是不可以使用new命令，否则会报错；箭头函数中不存在arguments对象

- 

- 

- 

- 

  

  

  

  

  