# 含义与工作方式，加速Features 

AfDelivr ，A fast CDN，稳中求快

相关设置：所有文件缓存60天，强制https

它的工作方式是这样的：
NPM加速服务：

通过镜像回源的方式，将请求文件储存至USS，（类似于jsd的处理方式，可参考此文章：[ADN加速服务工作流程](https://arcitcgn.cn/185.html)

并同时在国内同时接入腾讯云，百度云，又拍云加速多家CDN共同加速（后续我们会考虑仅接入一家CDN)，

负载均衡，为用户提供优质的加速体验，

在线Ping测试：
![](media/2.png)
![](media/3.png)
除部分西部地区外，平均延迟≤25ms，平均响应IP数量在48-65之间（可能出现变化，后续考虑单一接入CDN）.
![](media/4.png)

# 使用方法 
## 使用前，请您充分阅读并同意[AfDelivr公益服务使用协议](https://arcitcgn.cn/189.html)
## npm包使用方法

npm地址：
```
https://cdn.afdelivr.top/npm/包名@版本号/文件名
```
如何将资源上传到[npm](https://www.npmjs.com/)，可以参考以下两篇文章：

[npm图床的使用技巧](https://akilar.top/posts/3e956346/)

[利用GitHub Action自动发布你的静态资源到npm](https://bowenyoung.cn/posts/action-npm/)

## DNS预解析
DNS 预读取是一种使浏览器主动执行 DNS 解析以达到优化加载速度的功能。
将本加速服务融入DNS预解析，只需要在您网站的`<meta charset="UTF-8">`
后添加：
```
<link rel="dns-prefetch" href="//cdn.afdelivr.top" />
```

在此特别鸣谢[Teacher Du](https://dusays.com/)，[檐牙](https://www.zxma.top/)，[BeaCox](https://bowenyoung.cn/)，[Felix](https://www.felixchen0707.cn/)和[小邢同学](https://aboke.net/)，



## 赞助AfDelivr：如果您希望我们的项目更好地走下去，您可以赞助我们；您可以前往我们的[赞助页面](https://arcitcgn.cn/thanks.html)赞助我们
<img src="media/WechatPay.jpg" alt="微信支付" width="40%" align="left" /> <img src="media/Alipay.jpg" alt="支付宝" width="40%" align="right" />

