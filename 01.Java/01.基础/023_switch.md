# switch

```switch
switch(expression){

    case value :

        //语句

        break; //可选

    case value :

        //语句

        break; //可选

    //你可以有任意数量的case语句

    default : //可选

        //语句

}
```

* expression 支持类型

  基本数据类型：byte, short, int, char

  包装数据类型：Byte, Short, Integer, Character

  枚举类型：Enum

  字符串类型：String（Jdk 7+ 开始支持）

* case 只能是常量或者字面常量

* default 语句可有可无，最多只能有一个
