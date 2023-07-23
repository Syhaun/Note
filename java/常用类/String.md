# String
## 基本方法

length()

charAt(index)

concat(s) 
将该字符串和s连接，返回一个新的字符串

toUpperCase()

toLowerCase()

trim()
返回去掉了两边空白字符的新字符串
## 输入

next()方法
  读取以空白字符结束的字符串

nextLine() 
 读取以按下回车键结束的字符串
## 字符串比较

equals(s1)

equalsIgnoreCase(s1) 
 不区分大小写

compareTo(s1) 
 返回一个大于0，小于0，等于0的整数，分别表示该字符串是否大于，等于，小于s1(实际返回的是s1和s2从左到右第一个不同字符之间的偏移)

eg：s1 = abc;s2 = abg;
    s1.compareTo(s2) 返回 -4
## 获得子字符串

substring(beginIndex) 
返回从指定位置 beginIndex 到字符串的结束

substring(index1,index2) 
返回从下标为 index1 到 ==index2 - 1== 的子串

## 查找字符串中的字符或者子串
indexOf(ch) 
返回字符串中第一个出现ch的下标，没有返回-1

indexOf(ch,fromIndex)
   返回字符串中fromIndex之后出现的第一个ch的下标

indexOf(s) 

indexOf(s,fromIndex)

lastIndexOf(ch)
 返回最后一个出现ch的下标

lastIndexOf(ch,fromIndex)

lastIndexOf(s)

lastIndexOf(s,fromIndex)

### 替换和拆分字符串
replace(oldchar ,new char)

将老字符替换为新字符，然后返回新的字符串

replaceFirst(char1,char2)

replaceAll(String 1,String 2)

split(String) 

返回一个字符串数组，其中包含被分隔符拆分的字符串集

### 字符串与数组之间的转换

toCharArray()

将一个字符串转化成一个字符数组

构造方法 String(char[]) 或者方法valueOf(char[])

将字符数组转化为字符串