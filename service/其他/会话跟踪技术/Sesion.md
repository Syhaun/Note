# Session����ʹ��

Session:����˻Ự����,�����ݱ����ڷ����

JavaEE�ṩHttpSession�ӿ�,��ʵ�����λỰ�Ķ����������ݹ�����

1. ��ȡSession����
    `HttpSession session = request.getSession();`
2. Session������
   * `void setAttribute(String name,Object o);`�洢���ݵ�session����
   * `Object getAttribute(String name)`:����key,��ȡֵ
   * `void removeAttribute(String name):`����key,ɾ���ü�ֵ��

## Sessionԭ��

Session�ǻ���Cookieʵ�ֵ� 

![Alt text](image-1.png)

