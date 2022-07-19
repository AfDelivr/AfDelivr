## 为什么弄起了ADN这个项目？（在此先废话几句 ::aru:sweat:: ）##
听到[檐牙同学][1]的倾诉：“饿了么挂了，我的博客凉凉了”，内心是有点同情的，毕竟是自己苦心搭建的博客 ::aru:smile:: 
又听到了[Teacher DU][2]的建议，
![62d142ba15886.png][3]
再加上我这段时间也在想着做什么公益项目，
 ::aru:insidious:: ，没错，ADN公益加速从此诞生！

## 含义与工作方式，加速Feature ##

ADN，就是A fast CDN，稳中求快

相关设置：所有文件缓存60天，强制https

它的工作方式是这样的：
NPM加速服务：

通过镜像回源的方式，将请求文件储存至USS，（类似于jsd的处理方式，可参考此文章：[button color="success" icon="" url="https://arcitcgn.cn/185.html" type=""]ADN加速服务工作流程[/button]）

并同时在国内同时接入腾讯云，百度云，又拍云加速（和[深海图床][4]走的道路一样）多家CDN共同加速，

负载均衡，为用户提供优质的加速体验，

形成了**“全方位，多层次，高度可持续”**的加速格局。

[collapse status="false" title="如何理解“全方位，多层次，高度可持续”的加速格局"]
 1. 全方位：中国境内的所有地区（除部分少数民族地区外）都有加速节点分布，需要注意的是境外的所有来源都被屏蔽，指向127.0.0.1。
 2. 多层次：加速服务经历了由单一到多样，由境外到境内，由不稳定到稳定，由低速逐步推向高速的发展过程，加速途径也在不断扩大（DNS预解析，前端竞速等）。
 3. 高度可持续：开设赞助通道，按照实际使用状况扩大或缩小投入资金（与市场调节的机制一致，但参与调节的要素是使用状况）。
[/collapse]

在线Ping测试：
![62d1542c05b66.png][5]
![62d15437ed242.png][6]
除部分西部地区外，平均延迟≤25ms，平均响应IP数量在48-65之间（可能出现变化，后续考虑单一接入CDN），
![62d155a35f880.png][7]

## 使用方法 ##

npm地址：

    https://adn.arcitcgn.cn/npm/包名@版本号/文件名

如何将资源上传到[npm][8]，可以参考以下两篇文章：：
[button color="success" icon="" url="https://akilar.top/posts/3e956346/" type=""]npm图床的使用技巧 —— Akilarの糖果屋[/button]
[button color="success" icon="" url="https://bowenyoung.cn/posts/action-npm/" type=""]利用GitHub Action自动发布你的静态资源到npm —— Bowen Youngの破站[/button]
**小小的“黑科技”：**
DNS预解析：DNS 预读取是一种使浏览器主动执行 DNS 解析以达到优化加载速度的功能。
将本加速服务融入DNS预解析，只需要在您网站的`<meta charset="UTF-8">`
后添加：

    <link rel="dns-prefetch" href="//adn.arcitcgn.cn" />

## 结尾 ##

目前我就觉得这个公益坚持下面的“方针”:“以博客圈内使用为主，欢迎来使用者，服务一位是一位”

公益事业的蓬勃发展离不开我许多朋友的支持与帮助，

在此特别鸣谢@[Teacher Du][9],@[檐牙][10],@[BeaCox][11],@[Felix][12]和@[小邢同学][13]，

对于公益事业可能会出现的艰难险阻，我会尽自己一切力量地去战胜（也请各位网友规范使用，不要用做任何的非法用途），正如互联网总是在惊涛骇浪发展过来的！

补充：关于滥用行为

滥用指胡乱地或过度地使用，我们会在CDN后台追踪高流量使用的网页，判断其合法性；如出现滥用行为，我们会进行屏蔽“拉黑”处理。
各位网友如果遇到滥用CDN的行为，可向：i@arcitcgn.cn 发送邮件。

在此也希望能够造福各位博友！！谢谢



  [1]: https://www.zxma.top
  [2]: https://dusays.com
  [3]: https://oc.arcitcgn.cn/2022/07/15/62d142ba15886.png
  [4]: https://img.arcitcgn.cn
  [5]: https://oc.arcitcgn.cn/2022/07/15/62d1542c05b66.png
  [6]: https://oc.arcitcgn.cn/2022/07/15/62d15437ed242.png
  [7]: https://oc.arcitcgn.cn/2022/07/15/62d155a35f880.png
  [8]: https://www.npmjs.com/
  [9]: https://dusays.com
  [10]: https://www.zxma.top
  [11]: https://bowenyoung.cn/
  [12]: https://www.felixchen0707.cn/
  [13]: https://aboke.net
