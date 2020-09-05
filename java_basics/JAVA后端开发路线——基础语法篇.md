### 1. 一个简单的JAVA应用程序
```java
public class FirstSample
{
	public static void main(String[] args)
	{
		System.out.println("hello world!");
	}
}
```
程序执行后，控制台上将会显示`hello world!`  
### 2.注释
|符号|作用|
|----|----|
|//注释内容|其注释内容从//开始到本行末尾|
|/\*注释内容\*/|可以将一段比较长的注释括起来|
|/\*\*注释内容\*/|这种注释可以用来自动生成文档|
### 3.数据类型
java数据类型分为基本数据类型和引用数据类型。
**基本数据类型有int、short、long、byte、float、double、char、boolean**，其余数据类型都为引用数据类型，**引用数据类型的默认值为null**，常见的引用数据类型有：String，StringBuffer，ArrayList，HashMap等。

#### 3.1整型
|类型|存储需求|默认值|取值范围|
|----|----|----|----|
|int|4字节|0|-2 147 483 648 ~ 2 147 483 647(正好超过20亿)|
|short|2字节|0|-32 768 ~ 32767|
|long|8字节|0|-9 223 372 036 854 775 808 ~ 9223 372 036 854 775 807|
|byte|1字节|0|-128 ~ 127|
#### 3.2浮点类型
|类型|存储需求|默认值|取值范围|
|----|----|----|----|
|float|4字节|0.0f|大约±3.402 823 47E+38F|
|double|8字节|0.0d|大约±1.797 693 134 862 315 70E+308|

浮点数值不适用于无法接受舍入误差的金融计算中，如果在数值计算中不允许有任何舍入误差，就应该使用**BigDecimal**类
#### 3.3char类型
默认值：**'\u000'**  
char类型原本用于表示单个字符。不过，现在情况已经有所变化。Unicode打破了传统字符编码机制的限制。  
我们强烈建议不要在程序中使用char类型，除非确实需要处理UTF-16代码单元。最好将**字符串**作为抽象数据处理类型。

<center><font size=4>特殊字符的转义序列</font></center>

|转义序列|名称|Unicode值|
|----|----|----|
|\b|退格|\u0008|
|\t|制表|\u0009|
|\n|换行|\u000a|
|\r|回车|\u000d|
|\"|双引号|\u0022|
|\'|单引号|\u0027|
|\\ |反斜杠|\u005c|
#### 3.4boolean类型
默认值：**false**
boolean(布尔)类型有两个值：**false**和**true**，用来判断逻辑条件。整型值和布尔值之间不能进行互相转换。
#### 3.5数据类型之间的转换
* 合法转换

![数值类型之间的合法转换](..\pictures\数值类型之间的合法转换.png)

实心箭头表示无信息丢失的转换，虚箭头表示可能有精度损失的转换。
* 强制转换
double有时需要将double转换为int。
	
```java
double x = 9.997;
int nx = (int) x;
//变量nx的值为9
```
### 4变量与常量
* 类变量：独立于方法之外的变量，用 static 修饰。
* 实例变量：独立于方法之外的变量，不过没有 static 修饰。
* 局部变量：类的方法中的变量。
```java
public class Variable{
    static int allClicks=0;    // 类变量
    String str="hello world";  // 实例变量
    public void mehod(){
        int i =0;  // 局部变量
    }
}
```  

#### 4.1变量命名规范
变量名必须是一个以字母开头并由字母或数字构成的序列。大小写敏感。  
字母包括'A' ~ 'Z'、'a' ~ 'z'、'_'、'$'  
数字包括‘0~9’  
变量名不能是java中的保留关键字  

<center><font size=4>java中的保留关键字</font></center>
<table>
<thead>
<tr>
<th>访问控制</th>
<th>private</th>
<th>protected</th>
<th>public</th>
<th></th>
<th></th>
<th></th>
<th></th>
</tr>
</thead>
<tbody>
<tr>
<td>类，方法和变量修饰符</td>
<td>abstract</td>
<td>class</td>
<td>extends</td>
<td>final</td>
<td>implements</td>
<td>interface</td>
<td>native</td>
</tr>
<tr>
<td></td>
<td>new</td>
<td>static</td>
<td>strictfp</td>
<td>synchronized</td>
<td>transient</td>
<td>volatile</td>
<td></td>
</tr>
<tr>
<td>程序控制</td>
<td>break</td>
<td>continue</td>
<td>return</td>
<td>do</td>
<td>while</td>
<td>if</td>
<td>else</td>
</tr>
<tr>
<td></td>
<td>for</td>
<td>instanceof</td>
<td>switch</td>
<td>case</td>
<td>default</td>
<td></td>
<td></td>
</tr>
<tr>
<td>错误处理</td>
<td>try</td>
<td>catch</td>
<td>throw</td>
<td>throws</td>
<td>finally</td>
<td></td>
<td></td>
</tr>
<tr>
<td>包相关</td>
<td>import</td>
<td>package</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>基本类型</td>
<td>boolean</td>
<td>byte</td>
<td>char</td>
<td>double</td>
<td>float</td>
<td>int</td>
<td>long</td>
</tr>
<tr>
<td></td>
<td>short</td>
<td>null</td>
<td>true</td>
<td>false</td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>变量引用</td>
<td>super</td>
<td>this</td>
<td>void</td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>保留字</td>
<td>goto</td>
<td>const</td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>  

#### 4.2类变量  
* 类变量也称为静态变量，在类中以 static 关键字声明，但必须在方法之外。  
* 无论一个类创建了多少个对象，类只拥有类变量的一份拷贝。  
* 静态变量除了被声明为常量外很少使用，静态变量是指声明为 public/private，final 和 static 类型的变量。静态变量初始化后不可改变。  
* 静态变量储存在静态存储区。经常被声明为常量，很少单独使用static声明变量。  
* 静态变量在第一次被访问时创建，在程序结束时销毁。  
* 与实例变量具有相似的可见性。但为了对类的使用者可见，大多数静态变量声明为public类型。  
* 默认值和实例变量相似。数值型变量默认值是0，布尔型默认值是false，引用类型默认值是null。变量的值可以在声明的时候指定，也可以在构造方法中指定。此外，静态变量还可以在静态语句块中初始化。  
* 静态变量可以通过：ClassName.VariableName的方式访问。  
* 类变量被声明为public static final类型时，类变量名称一般建议使用大写字母。如果静态变量不是public和final类型，其命名方式与实例变量以及局部变量的命名方式一致。  
#### 4.3实例变量  
* 实例变量声明在一个类中，但在方法、构造方法和语句块之外；  
* 当一个对象被实例化之后，每个实例变量的值就跟着确定；  
* 实例变量在对象创建的时候创建，在对象被销毁的时候销毁；  
* 实例变量的值应该至少被一个方法、构造方法或者语句块引用，使得外部能够通过这些方式获取实例变量信息；  
* 实例变量可以声明在使用前或者使用后；  
* 访问修饰符可以修饰实例变量；  
* 实例变量对于类中的方法、构造方法或者语句块是可见的。一般情况下应该把实例变量设为私有。通过使用访问修饰符可以使实例变量对子类可见；  
* 实例变量具有默认值。数值型变量的默认值是0，布尔型变量的默认值是false，引用类型变量的默认值是null。变量的值可以在声明时指定，也可以在构造方法中指定；  
* 实例变量可以直接通过变量名访问。但在静态方法以及其他类中，就应该使用完全限定名：ObejectReference.VariableName。  
#### 4.4局部变量  
* 局部变量声明在方法、构造方法或者语句块中；  
* 局部变量在方法、构造方法、或者语句块被执行的时候创建，当它们执行完成后，变量将会被销毁；  
* 访问修饰符不能用于局部变量；  
* 局部变量只在声明它的方法、构造方法或者语句块中可见；  
* 局部变量是在栈上分配的。  
* 局部变量**没有默认值**，所以局部变量被声明后，必须经过初始化，才可以使用。  
#### 4.5常量  
在Java中，利用关键字final指示常量。关键字final表示这个变量只能被赋值一次。一旦被赋值以后，就不能再被更改了。习惯上，常量名使用全大写。  
在Java中，经常希望某个常量可以在一个类中的多个方法中使用，通常将这些常量称为类常量。可以使用关键字 static final 设置一个类常量，类常量定义于main方法的外部。  
### 5运算符
#### 5.1算术运算符
<table><tbody>
		<tr><th>操作符</th>
			<th>描述</th>
			<th>例子</th>
		</tr><tr><td>+</td>
			<td>加法</td>
			<td>10 + 20 等于 30</td>
		</tr><tr><td>-</td>
			<td>减法</td>
			<td>10 – 20 等于 -10</td>
		</tr><tr><td>*</td>
			<td>乘法</td>
			<td>10 * 20等于200</td>
		</tr><tr><td>/</td>
			<td>除法 (舍去余数)</td>
			<td>15 / 7等于2</td>
		</tr><tr><td>％</td>
			<td>取余(取模)</td>
			<td>15%7等于1</td>
		</tr><tr><td>++</td>
			<td>自增: 操作数的值增加1</td>
			<td>20++ 或 ++20 等于 21</td>
		</tr><tr><td>--</td>
			<td>自减: 操作数的值减少1</td>
			<td>20-- 或 --20 等于 19</td>
		</tr>
</tbody></table>  

* 整数被0除会产生一个异常，而浮点数被0除将会得到无穷大或NaN结果。  
* x++前缀形式会先完成加一，而++x后缀形式会使用变量原来的值。  
```java
int m = 7;
int n = 7;
int a = 2 * ++m;//a为16，m为8
int b = 2 * n++;//b为14，n为8
```
建议不要在表达式中使用++，不易读且易出bug。

#### 5.2位运算符
设a = 60 (0011 1100)，b = 13 (0000 1101)
<table><tbody>
		<tr><th>操作符</th>
			<th>描述</th>
			<th>例子</th>
		</tr><tr><td>＆</td>
			<td>如果相对应位都是1，则结果为1，否则为0</td>
			<td>（A＆B），得到12，即0000 1100</td>
		</tr><tr><td>|</td>
			<td>如果相对应位都是0，则结果为0，否则为1</td>
			<td>（A | B）得到61，即 0011 1101</td>
		</tr><tr><td>^</td>
			<td>如果相对应位值相同，则结果为0，否则为1</td>
			<td>（A ^ B）得到49，即 0011 0001</td>
		</tr><tr><td>〜</td>
			<td>按位取反运算符翻转操作数的每一位，即0变成1，1变成0。</td>
			<td>（〜A）得到-61，即1100 0011</td>
		</tr><tr><td>&lt;&lt;&nbsp;</td>
			<td>按位左移运算符。左操作数按位左移右操作数指定的位数。</td>
			<td>A &lt;&lt; 2得到240，即 1111 0000</td>
		</tr><tr><td>&gt;&gt;&nbsp;</td>
			<td>按位右移运算符。左操作数按位右移右操作数指定的位数。</td>
			<td>A &gt;&gt; 2得到15即 1111</td>
		</tr><tr><td>&gt;&gt;&gt;&nbsp;</td>
			<td>按位右移补零操作符。左操作数的值按右操作数指定的位数右移，移动得到的空位以零填充。</td>
			<td>A&gt;&gt;&gt;2得到15即0000 1111</td>
		</tr>
</tbody></table>

#### 5.2结合赋值和运算符
x += 4 等价于 x = x + 4  
一般的，要把运算符放在 = 号左边，如 *= 或 %=。  
#### 5.3关系运算符  
设A为10，B为20.  
<table><tbody>
		<tr><th>运算符</th>
			<th>描述</th>
			<th>例子</th>
		</tr><tr><td>==</td>
			<td>检查如果两个操作数的值是否相等，如果相等则条件为真。</td>
			<td>（A == B）为假。</td>
		</tr><tr><td>!=</td>
			<td>检查如果两个操作数的值是否相等，如果值不相等则条件为真。</td>
			<td>（A != B） 为真。</td>
		</tr><tr><td>&gt;&nbsp;</td>
			<td>检查左操作数的值是否大于右操作数的值，如果是那么条件为真。</td>
			<td>（A&gt; B）为假。</td>
		</tr><tr><td>&lt;&nbsp;</td>
			<td>检查左操作数的值是否小于右操作数的值，如果是那么条件为真。</td>
			<td>（A &lt;B）为真。</td>
		</tr><tr><td>&gt;=</td>
			<td>检查左操作数的值是否大于或等于右操作数的值，如果是那么条件为真。</td>
			<td>（A&gt; = B）为假。</td>
		</tr><tr><td>&lt;=</td>
			<td>检查左操作数的值是否小于或等于右操作数的值，如果是那么条件为真。</td>
			<td>（A &lt;= B）为真。</td>
		</tr>
</tbody></table>  
#### 5.4逻辑运算符  
设布尔值A为真，B为假  
<table><tbody>
		<tr><th>操作符</th>
			<th>描述</th>
			<th>例子</th>
		</tr><tr><td>&amp;&amp;</td>
			<td>称为逻辑与运算符。当且仅当两个操作数都为真，条件才为真。</td>
			<td>（A &amp;&amp; B）为假。</td>
		</tr><tr><td>| |</td>
			<td>称为逻辑或操作符。如果任何两个操作数任何一个为真，条件为真。</td>
			<td>（A | | B）为真。</td>
		</tr><tr><td>！</td>
			<td>称为逻辑非运算符。用来反转操作数的逻辑状态。如果条件为true，则逻辑非运算符将得到false。</td>
			<td>
			<p>!（A &amp;&amp; B）为真。</p>
			</td>
		</tr>
</tbody></table>  
#### 5.5三元运算符  
condition ? expression1:expressionw2  
如果condition为true，则返回expression1，如果condition为false，则返回expression2.  

```java
//设x=1，y=2
x < y ? x : y4
//结果会返回x
```  
#### 5.6运算符的优先级
<table><tbody>
		<tr><th>类别</th>
			<th>操作符</th>
			<th>优先级</th>
		</tr><tr><td>后缀</td>
			<td>() [] . (点操作符)</td>
			<td>左到右</td>
		</tr><tr><td>一元</td>
			<td>+ + - ！〜</td>
			<td>从右到左</td>
		</tr><tr><td>乘性&nbsp;</td>
			<td>* /％</td>
			<td>左到右</td>
		</tr><tr><td>加性&nbsp;</td>
			<td>+ -</td>
			<td>左到右</td>
		</tr><tr><td>移位&nbsp;</td>
			<td>&gt;&gt; &gt;&gt;&gt; &nbsp;&lt;&lt;&nbsp;</td>
			<td>左到右</td>
		</tr><tr><td>关系&nbsp;</td>
			<td>&gt;&gt; = &lt;&lt; =&nbsp;</td>
			<td>左到右</td>
		</tr><tr><td>相等&nbsp;</td>
			<td>==&nbsp; !=</td>
			<td>左到右</td>
		</tr><tr><td>按位与</td>
			<td>＆</td>
			<td>左到右</td>
		</tr><tr><td>按位异或</td>
			<td>^</td>
			<td>左到右</td>
		</tr><tr><td>按位或</td>
			<td>|</td>
			<td>左到右</td>
		</tr><tr><td>逻辑与</td>
			<td>&amp;&amp;</td>
			<td>左到右</td>
		</tr><tr><td>逻辑或</td>
			<td>| |</td>
			<td>左到右</td>
		</tr><tr><td>条件</td>
			<td>？：</td>
			<td>从右到左</td>
		</tr><tr><td>赋值</td>
			<td>= + = - = * = / =％= &gt;&gt; = &lt;&lt; =＆= ^ = | =</td>
			<td>从右到左</td>
		</tr><tr><td>逗号</td>
			<td>，</td>
			<td>左到右</td>
		</tr>
</tbody></table>
### 6字符串
```

```
