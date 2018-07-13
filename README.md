# yangAjax

## 如何使用
1、下载放在一个文件夹里，然后调用或使用npm进行下载
``` bash
npm install longajax --save

```

或者下载该文件，引入
``` bash
<script src="yangAjax.js"></script>
```

2、在Vue中使用

1）在main.js引入
``` bash

var longajax = require('longajax');

或

import longajax from 'longajax';

Vue.prototype.ajax = (config) => {
     longajax(config);
}

```
2） 在其他组件中使用
``` bash
this.ajax({
     url:'your url',  // 接口路径
     method:'your method',  //方法  POST/GET
     dataType:'json',       // 数据类型
     async:true,           // 异步  true/false
     data:data,            // 传递的数据
     success: (ret , message , status) =>{   // 成功
           console.log(ret);
     },
     fail: (status , statusText ) =>{   // 失败
            console.log(status);
     }
});
```

3、 在React中使用

1）在main.js引入
``` bash

import {yangAjax} from 'longajax';

React.ajax = yangAjax;

```
2） 在其他组件中使用
``` bash
ajax({
     url:'your url',  // 接口路径
     method:'your method',  //方法  POST/GET
     dataType:'json',       // 数据类型
     async:true,           // 异步  true/false
     data:data,            // 传递的数据
     success: (ret , message , status) =>{   // 成功
           console.log(ret);
     },
     fail: (status , statusText ) =>{   // 失败
            console.log(status);
     }
});
```

## 注意

可搭配FormData使用，用来实现图片无刷新上传
