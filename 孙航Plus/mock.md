## `Mock`

* 官网: http://mockjs.com
* 文档: https://github.com/nuysoft/Mock/wiki

* `mockjs` 随机生成数据



#### 安装mock

```js
npm install mockjs
```



#### mock简单使用

```js
const Mock = require("mock")

const data = Mock.mock({
    `result|4`:[
    	{
			'id|+1':1,
    		'name':'小梦'
        }
    ]
})
//JSON.stringify(数据,数据转换函数,缩进空格数)
JSON.stringify(data,null,4)
```



#### 语法规则

* mock数据包含两部分

1. 数据模板定义: `DTD`
2. 数据占位符定义:`DPD`



#### 数据模板定义

* __数据模板由3部分组成: 属性名,生成规则,属性值__

```js
// 属性名|生成规则: 属性值
'name|rule': value
```

* 属性名与生成规则之间以|隔开
* 生成规则一共有7种 

1. 'name|+step': value   生成递增数据
2. 'name|count': value 生成固定数量数据
3. 'name|min-max': value  生成指定范围之内的数据
4. `'name|min-max.dmin-dmax'`: value 生成指定范围之内的小数  小数的位数范围是 `dmin-dmax`
5. `'name|min-max.dcount': value `
6. `'name|count.dcount:' value`
7. `'name|count.dmin-dmax:' value`

* 属性值可以使用 @占位符
* 属性值指定了最终的初始值和类型
  * 属性值为boolean类型 : 
    * `name|1:true`  指的是生成概率为1/2
    * `name|2-4:true`  指的是生成true的概率为2/(2+4),false的概率为4/(2+4)
  * 属性值为Object类型:
    * 'name|count: object' 从object中随机选择count个属性
    * 'name|min-max: object' 从object中随机选择 min到max个属性
  * 属性值是Array类型:
    * 'name|min-max: array'  随机生成min-max个元素
  * 属性值为`RegExp`类型:
    * 'name':` regexp `
    * __注意: `regexp`是没有双引号的__



#### 数据占位符定义

`Mock.random`是一个工具, 用于生成随机数据

这个方法称为 [占位符] , 书写方式是 @占位符(参数,[参数])

```js
'属性名': @占位符
```

| type类型      | Method(占位符)                                               |
| :------------ | ------------------------------------------------------------ |
| Basic         | boolean,natural,integer,float,character,string,range(整形数组) |
| Date          | `date,time,datetime`                                         |
| image         | `image,dataimage`                                            |
| Color         | color                                                        |
| Text          | `paragraph,sentence,word,title,cparagraph,csentence,cword,ctitle` |
| Name          | `first,last,name,cfirst,clast,cname`                         |
| Web           | `url,domain,email,ip,tld`                                    |
| `Addrss`      | area,region,zip,country                                      |
| Helper        | capitalize,upper,lower,pick,shuffle                          |
| Miscellaneous | `guid,id`                                                    |

