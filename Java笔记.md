# Java笔记
---
## 整型转换为字符串
 - `int i = Integer.parseInt(String);`
 - `int i = Integer.valueOf(String).intValue();`

parseInt()是把String变成int的基础数据类型;
valueOf()是把给定的String参数转化成Integer对象类型;
intValue()是把Integer对象类型变成int的基础数据类型;
## 字符串转换为整型

 - `String str = String.valueOf(int);`
 - `String str = String.toString(int);`
 - `String s = "" + int;`

---
## 数组转换为字符串##
### char数组转换为字符串
    char[] charArray = {'a','b','c'};
    String str = String.copyValueOf(charArray);
    System.out.println(str);
### String数组转换为字符串
    String[] strArray = {"123","abc","321"};
    StringBuffer sb = new StringBuffer();
    for(int i = 0; i < strArray.length; i++){
        sb.append(strArray[i]);
    }
    String newStr = sb.toString();
    System.out.println(newStr);
## 字符串转换为数组
    String str = "123abc";
    char[] charArray = str.toCharArray();
    for(int i = 0; i < charArray.length; i++){
        System.out.println(charArray[i]);
    }
## 其他转换
### 字符串逆序
    String str = "123abc";
    System.out.println(new StringBuilder(str).reverse().toString());
### 字符串去空格
#### 常用空白字符：
空格(' ') 、换页 ('\f') 、换 行('\n')、回车('\r')、水平制表符 ('\t')、垂直制表符 ('\v')

 - `String.trim()`
 - `String.replaceAll(" ","");`
 - `String.replacaAll("\\s*","");`

