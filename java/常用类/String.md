# String
## ��������

length()

charAt(index)

concat(s) 
�����ַ�����s���ӣ�����һ���µ��ַ���

toUpperCase()

toLowerCase()

trim()
����ȥ�������߿հ��ַ������ַ���
## ����

next()����
  ��ȡ�Կհ��ַ��������ַ���

nextLine() 
 ��ȡ�԰��»س����������ַ���
## �ַ����Ƚ�

equals(s1)

equalsIgnoreCase(s1) 
 �����ִ�Сд

compareTo(s1) 
 ����һ������0��С��0������0���������ֱ��ʾ���ַ����Ƿ���ڣ����ڣ�С��s1(ʵ�ʷ��ص���s1��s2�����ҵ�һ����ͬ�ַ�֮���ƫ��)

eg��s1 = abc;s2 = abg;
    s1.compareTo(s2) ���� -4
## ������ַ���

substring(beginIndex) 
���ش�ָ��λ�� beginIndex ���ַ����Ľ���

substring(index1,index2) 
���ش��±�Ϊ index1 �� ==index2 - 1== ���Ӵ�

## �����ַ����е��ַ������Ӵ�
indexOf(ch) 
�����ַ����е�һ������ch���±꣬û�з���-1

indexOf(ch,fromIndex)
   �����ַ�����fromIndex֮����ֵĵ�һ��ch���±�

indexOf(s) 

indexOf(s,fromIndex)

lastIndexOf(ch)
 �������һ������ch���±�

lastIndexOf(ch,fromIndex)

lastIndexOf(s)

lastIndexOf(s,fromIndex)

### �滻�Ͳ���ַ���
replace(oldchar ,new char)

�����ַ��滻Ϊ���ַ���Ȼ�󷵻��µ��ַ���

replaceFirst(char1,char2)

replaceAll(String 1,String 2)

split(String) 

����һ���ַ������飬���а������ָ�����ֵ��ַ�����

### �ַ���������֮���ת��

toCharArray()

��һ���ַ���ת����һ���ַ�����

���췽�� String(char[]) ���߷���valueOf(char[])

���ַ�����ת��Ϊ�ַ���