﻿# WebRunLocal
       WebRunLocal(本网通)是一个实现浏览器网页与本地程序之间进行双向调用的轻量级、强兼容、可扩展的插件开发平台。
通过本网通可实现网页中的JavaScript脚本无障碍访问本地电脑的硬件、调用本地系统的API及相关组件，同时彻底解决ActiveX组件在Chrome、FireFox、Opera、Edge、Safari等浏览器各版本中的兼容使用问题。

系统兼容性：
1、全面兼容Windows XP、Vista、7、8、10各版本桌面系统；
2、全面兼容Windows Server 2003、2008、2012、2016各版本服务器系统；
3、Linux、Mac、安卓等系统暂不支持，技术上可实现，欢迎伙伴的参与。

浏览器兼容性：
1、IE 8及以上版本；
2、Chrome 16及以上版本；
3、FireFox 11及以上版本；
4、Safari 7及以上版本；
5、Opera 12.1及以上版本；
6、Edge 12及以上版本。

      在IE中实现网页和本地系统双向调用的方法是使用ActiveX控件技术，而在Chrome、FireFox等浏览器有类似的NPAPI插件技术。因为安全隐患及稳定性等问题，微软新生代浏览器Edge不再支持ActiveX控件，目前主流的Chrome浏览器也从42版开始NPAPI插件被抛弃，导致原来很多依赖这些技术实现的业务无法在新版浏览器中继续使用。

目前浏览器网页与本地程序之间双向调用的知名解决方案有以下两个：
1、firebreath，核心实现采用的是ActiveX控件和NPAPI插件技术，已面临新版浏览器不能全面兼容使用的问题；
2、Node.js，是一个基于Chrome V8引擎的 JavaScript 运行环境，其中FFI模块可实现在JavaScript中调用本地C语言风格的动态链接库。运行及部署依赖Python和npm，另外需要区别处理32位和64位的程序调用，尤其是不能支持ActiveX控件等面向对象的组件调用。

使用WebRunLocal(本网通)的理由：
1、轻量级：本网通整个程序包很小，不再依赖其它第三方程序即可使用；
2、强兼容性：本网通采用HTML5标准中的Web Socket技术，可确保在各个浏览器版本的兼容使用；
3、本网通在Windows平台采用COM组件技术为上层插件开发提供友好的集成支持；
4、自定义的可配置和程序分发支持，方便基于本网通的第三方集成使用。

使用场景举例：
1、网页中需要和本地电脑的硬件进行交互，比如B/S架构的OA系统中操作本地打印机；
2、网页中需要调用本地程序的ActiveX控件实现一些特殊服务，比如Office文档的在线预览和编辑；
3、一些软件系统使用了第三方的DLL模块，可通过本网通实现在B/S架构中的系统中调用；
4、网银、在线支付等安全性要求高的网站，可基于本网通开发访问U盾等的加密模块提供访问安全性。
