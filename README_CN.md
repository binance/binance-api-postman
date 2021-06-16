# Binance API Postman

[Postman](https://getpostman.com) 是一个API合作平台。

为了便于用户快速方便的使用RESTful，币安提供几个`Postman`的`Collection`.<br/>
同时我们还提供`environment`文件， 可以方便的导入。换上用户自己的Key就可以直接使用。

## 如何导入`Collection`
- 下载`Collection`文件到本地
- 导入到Postman中

## 如果导入`environment`文件
- 下载`environment`文件到本地。
- 以Mac版的Postman为例， 点击右上角的按钮`Manage Environments`(齿轮图标)
    <p align="center"><img src="https://raw.githubusercontent.com/binance-exchange/binance-api-postman/assets/postman/1.png"/></p>
- 从弹出来的窗口，点击导入按钮(`import`), 然后选择上面下载好的`environment`文件。
   <p align="center"><img src="https://raw.githubusercontent.com/binance-exchange/binance-api-postman/assets/postman/2.png"/></p>
- 点击进入刚才的配置文件，设置`API key`和`Secret key`，`timestamp`和`signature`留空就好。记得输入到`Current Value`里面，不然postman会上传到你的postman账号里面。确认退出。
    <p align="center"><img src="https://raw.githubusercontent.com/binance-exchange/binance-api-postman/assets/postman/3.png"/></p>
    
- 在右上角的下拉菜单里面找到刚才导入的配置, 然后就可以直接适用各个接口了。
    <p align="center"><img src="https://raw.githubusercontent.com/binance-exchange/binance-api-postman/assets/postman/4.png"/></p>

## FAQ
### 错误: `Could not get any response`
- 你没有设置`environment`，或者设置了没有选中。请按照上面的步骤设置好`environment`.

### 错误: `API-key format invalid.`
- `API key` 没有设置.
- `API key`不正确.
- Postman的`Headers`里面的`X-MBX-APIKEY`没有选中.

### 错误: `Signature for this request is not valid.`
有几种可能性:
- `Secret key`没有设置。
- 选中的参数没有赋值。如果不需要的参数，请不要选中。
- `signature`参数不在参数列表的最后。

### 错误: `Mandatory parameter 'xxxx' was not sent, was empty/null, or malformed.`
- 没有传入必须的参数。请参看API文档，里面参数的详细说明。

### 如何debug或者怎么查看请求的URL
- 打开Postman的控制台`(CMD/CTRL + ALT + C)`, 每一个请求都会打印出参数和URL。
- 编辑`Pre-request`脚本，方便调试。

## `Postman`安全吗？
我们建议用户自己写脚本调用API。但是用Postman可以尽快体验API的各个接口。有一些建议的最佳实践，供参考：
- 不要使用未知来源的`collections`.
- 使用前查看一下`collections`文件源码.
- 如果有不明白的代码，请不要使用。
- 生成`API key`, 不要给提款的权限。
- 试用后，尽快删除`API key`。

## 有疑问
请提[`issue`](https://github.com/binance-exchange/binance-api-postman/issues).

## License
MIT
