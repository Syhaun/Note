#swith 语法完整语法：
```
switch（switch表达式）{
    case value1: 语句1;break;
    case value: 语句2;break;
    default: 默认情况下执行的语句;
}
```
1. switch 表达式必须得到一个char，byte，short，int，或者String型值
2. value1 等必须和 switch 表达式的值具有相同的数据类型
3. 当swich 表达式的值和 case 语句的值匹配时，执行从 case 开始的语句，直到遇到一个 break 语句或者到达该 switch 语句的末尾
