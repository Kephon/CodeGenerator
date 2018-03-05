# CodeGenerator
CodeGenerator
mybatis代码生成器

mybatis 插件自动生成mapper接口以及xml文件的基础上，进行了封装，使用了通用的mapper增删改查，类型JPA的操作，继承了通用mapper；

除了mapper接口和xml映射文件生成以外，还可以自动生成service接口以及实现类，实体类，dto数据传输类，controller类

使用方式简单易懂，修改数据库配置文件，配置上自己的数据库地址，在数据库中创建一个自己想要的表以及字段，在test包下找到CodeGenerator类，在main方法中修改自己的表名， 一定要和自己数据库的表名一致，四个参数，第一个是要生成的表名，第二个是自定义名称（基本不用给参数），第三个是类注释，第四个是表主键的类型（基本都是int类型ID）

如果是多表一起生成，使用main方法中的另一个数组，可添加多表一起生成

若是要把在自己项目中添加这个自动生成的话，只需要全部拷贝过去，包括pom.xml，修改各部分的包名，修改ProjectConstant类型的生成路径，还有CodeGenerator类里数据库的配置地址以及创建人，其余不用修改即可。

PS：日志打印已经配置，修改logback.xml最底部标签里自己包路径即可，打印日志的作用是打印前端传入的参数在sql中实现的语句是怎么样的，以及程序运行时的sql状态