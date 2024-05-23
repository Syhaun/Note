# lombok

**LOmbok是一个实用的Java类库,能够通过注解的形式自动生成构造器,getter/setter,equals,hashcode,toString等方法,并可以自动化生成日志变量,简化java开发,提高效率**

|注释|作用|
|---|---|
|@Getter/@Setter|为所有的属性提供get/set方法|
|@ToString|会给类自动生成易阅读的toString方法|
|@EqualsAndHashCode|根据类所拥有的非静态字段自动重写equals方法和hashCode方法|
|@Data|提供了更综合的生成代码功能(@Getter+@Setter+@ToString+@EqualsAndHashCode)|
|@NoArgsConstructor|为实体类生成无参的构造器方法|
|@AllArgsConstructor|为实体类生成除了static修饰的字段之外带有各参数的构造器方法|

* Lombok会在编译时,自动生成对应的java代码
