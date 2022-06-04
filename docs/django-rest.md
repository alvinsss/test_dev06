# REST 框架

接口的实现风格

http协议 实现接口的时候

get/post/put/delete ....

get/post

* get  
  /api/user?id=1&name=tom
  /api/add?text="asdfasdf...."
  /api/login?username=admin&password=abc123

* post
  /api/add
  from-data/ body(JSON)
  /api/login

get + /api/user/query?id=1  查询
post + /api/user/update  更新
    form-data OR JSON
get + /ap/user/delete?id=1 


## REST 风格

* get  查询
get + /api/user/1/

* post 添加
post + /api/user/
  form-data OR JSON

* put  更新
put + /api/user/1/
   form-data OR JSON

* delete 删除
delete  + /api/user/1/


## REST 框架

django 模板 - 废掉了

django 专注去实现接口就好了。

* django-rest-framework


```json
{
    "success": true
    "error": {
        "code": 10023,
        "message": "用户id 不能为空"
    }
    "data": [
        ...
    ]
}
```

## fastapi 

* 专注于做后端API , 没有集成模板。
* 类似于 flask 风格（路由和视图绑定）

```py
from flask import Flask

app = Flask(__name__)

@app.route("/hello",  methods=['GET'])
def hello_world():
    return "<p>Hello, World!</p>"
```

* 自动生成Api文档 （代码即文档）

* 集成 pydantic 实现参数校验


添加用户的接口

```json
{
    "name": "adfasd",
    "age": 111,

}
```

name 是否必传，类型-字符串
age  是否必传，类型-整型

```py
class Item(BaseModel):
    name: str
    age: int = None
```

## django-ninja

* ninja 忍者

* django-ninja: 基于django框架的fastapi。

django 优点：
1. 集成ORM
2. 自带admin后台

fastapi 优点
1. 自动生成api
2. 类型校验
3. 异步，性能好

django-ninja = django + fastapi 



## 基础知识

http 协议

公路： 摩托车，电动汽车，大卡车，小汽车，大巴....

接口：

专用货车：  --> 水果批发市场 

