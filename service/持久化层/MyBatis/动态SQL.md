# ��̬SQL

�����û���������ⲿ�����ı仯���仯��SQL���,���ǳ�Ϊ��̬SQL

## if
 < if>: �����ж������Ƿ����.ʹ��test���Խ��������ж�,�������Ϊ true,��ƴ�� SQL

 ![Alt text](image-12.png)

 ## where

 < where>: whereԪ��ֻ������Ԫ�������ݵ�����²Ų���where�־�,���һ��Զ�ȥ���Ӿ�Ŀ�ͷ��AND��or

 ![Alt text](image-13.png)

 ## set

 < set>: ��̬�������ײ���SET�ؼ���,����ɾ������Ķ���.(����update�����)

 ```xml
   <update id="update">
        update tb_brand
        <set>
            <if test="brandName != null and brandName != ''">
                brand_name = #{brandName},
            </if>
            <if test="companyName != null and companyName != ''">
                company_name = #{companyName},
            </if>
            <if test=" ordered != null and  ordered != ''">
                ordered = #{ordered},
            </if>
            <if test="description != null and description != ''">
                description = #{description},
            </if>
            <if test="status != null">
                status = #{status}
            </if>
        </set>  
        where id = #{id};
    </update>
 ```

 ## foreach

 ![Alt text](image-14.png)

## choose(when,otherwise)

ѡ��������switch���
 
```xml
<select id="selectByConditionSingle" resultMap="brandResultMap">
        select *
        from tb_brand
        where
            <choose>
                <when test="status != null">
                 status = #{status}
                </when>
                <when test="companyName != null and companyName != ''">/*�൱��case*/
                    company_name like #{companyName}
                </when>
                <when test="brandName != null and brandName != ''">/*�൱��case*/
                    brand_name like #{brandName}
                </when>
                <otherwise>/*�൱��default*/
                    1 = 1 /* �������ʺϵ�Ĭ������ */
                </otherwise>
            </choose>
    </select>

```