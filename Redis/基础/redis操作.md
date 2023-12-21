# redis �����ݽṹ

Redis ��һ��key-value�����ݿ�,keyһ����String����,����value�����Ͷ��ֶ���

![Alt text](image-9.png)

# Redisͨ������

[�ٷ��ĵ���ѯ](https://redis.io/commands/)

����ڲ�ѯ

![Alt text](image-10.png)

* KEYS:�鿴����ģ�������key(����������������ʹ��)

![Alt text](image-11.png)

* DEL:ɾ��һ��ָ����key(����ֵ����ɹ�ɾ��������)

![Alt text](image-12.png)

* EXISTS:�ж�һ��key�Ƿ����(1��0��)

![Alt text](image-14.png)

* EXPIRE:��һ��key������Ч��,��Ч�ڵ���ʱkey�ᱻ�Զ�ɾ��

![Alt text](image-15.png)

* TTL:�鿴һ��KEY��ʣ����Ч��

![Alt text](image-16.png)

    1.����ֵΪ -2,��ʾ������Ч�ڵ�key��Ч�ڽ���
    2.����ֵΪ -1,��ʾ������Ч

==key�Ľṹ==

Redis��key�����ֶ�������γɲ㼶����,�������֮����:����

![Alt text](image-19.png)

![Alt text](image-20.png)

# ��ͨ��ָ��

## String����

String����,�ַ�������,redis����򵥵Ĵ洢����,value���ַ���,�����ַ����ĸ�ʽ��ͬ,��Ϊ3��

* string:��ͨ�ַ���
* int:����������,���������Լ�
* float:��������,���������Լ�

������һ�ָ�ʽ,�ײ㶼���ֽ�������ʽ�洢,���뷽ʽ����.

![Alt text](image-17.png)

## Hash����

Hash����,Ҳ��ɢ��,��value��һ�������ֵ�,������java�е�HaahMap�ṹ

![Alt text](image-21.png)

![Alt text](image-22.png)

## List����

Redis�е�list������java��linkedList����,���Կ�����һ��˫������ṹ.������֧���������Ҳ����֧�ַ������


����:����;Ԫ�ؿ����ظ�;�����ɾ����;��ѯ�ٶ�һ��

![Alt text](image-23.png)

![Alt text](image-24.png)


## set ����

Redis��set�ṹ��java�е�hashset����,���Կ���һ��valueΪnull��hashmap.

����: ����,Ԫ�ز����ظ�,���ҿ�,֧�ֽ���,����,��ȹ���

![Alt text](image-25.png)

## sortedSet����

Redis��SortedSet��һ�������򼯺�,��java�е�TreeSet����,���ǵײ����ݽṹ���ܴ�.SortedSet�е�ÿһ��Ԫ�ض�����һ��score����,���Ի���score���Զ�Ԫ������,�ײ��ʵ����һ�������hash��.

����:������;Ԫ�ز��ظ�;��ѯ�ٶȿ�(���ڿ����������,����������ʵ�����а������Ĺ���)

![Alt text](image-26.png)

**���е������Ͷ�������,���Ҫ������Ҫ�������z�������REV**




