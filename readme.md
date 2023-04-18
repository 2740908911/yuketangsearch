# yuketangSearch V3.0

<!--more-->

名称：雨课堂快速搜题工具 V3.0

记录时间：2022年12月19日

最后更新：2023年4月18日

作者：Fanqie（**别忘了STAR！！！**）

---

**下面是一份简单的使用说明：**

## 功能介绍

顾名思义，雨课堂作业发下来后快速搜题，不用再一个个ocr识别、打字、拍照，百度搜索等，

基本符合懒人需求（like me）

有啥好的建议也可以提issue

## 特性介绍

* 简化性
  * 为了大家开箱即用，直接编译好了exe，不用准备python环境
  * 直接生成网页链接，点击即跳转，想查哪道查哪道！
  * **v3内置了NewBingAI，GPT4同款，一键CHAT！！**（配置bingAI需要一定的计算机基础）
* 安全性
  * 雨课堂cookie和bing_cookie全部本地存储，只做网站访问用，不会窃取用户信息。
  * 不用打开控制台，防止雨课堂检测！
  * bing线程控制、日志记录、延迟控制，有效防封号！
* 二创性
  * 会生成题目文件，用其他搜题软件直接整页拍照，或者直接复制搜索，很方便！
  * 可以把导出的题目二次开发连接题库进行搜索
* 懒得编了，反正自己尝试吧

## 使用说明V3.0

* 工具预配置（若不使用bingAI搜索答案则可忽略部分配置）

  * 浏览器插件部分：

    ![7](http://img.imfanqie.top/program/ykt/7.png)

  * NewBing部分：

    * 请确保账户已经通过NewBing申请
    * 请确保账户能正常使用Chat功能

  * 代理部分：

    * 此部分为小白准备，若您能正常访问Chat功能，可以略看此部分。

    * VPN：此处使用艾可云；代理工具：clash for windows

    * 在艾可云官网拉入clash配置

      ![8](http://img.imfanqie.top/program/ykt/8.png)

    * 测速，全局和规则均使用延迟低的美国节点（日本节点）

      ![9](http://img.imfanqie.top/program/ykt/9.png)

    * 配置常规页面（抓取bing_cookie时使用系统代理，其他情况一律不使用）：

      ![10](http://img.imfanqie.top/program/ykt/10.png)

  ---

* 脚本配置：

  * 配置文件在目录config.yml中，同时需要配置cookies.json文件。

    ![11](http://img.imfanqie.top/program/ykt/11.png)

    * 配置文件已经默认配置好，若不确定请勿更改！
    * bing_proxy代理与clash上端口对应请勿随意修改！
    * 雨课堂信息部分可以为空，会在运行时填写；若在配置文件中填写，则默认使用配置文件中的信息！

  * cookies_json文件及cookie获取：

    ![12](http://img.imfanqie.top/program/ykt/12.png)

    * cookie获取：打开全局代理，访问newbing，更改地区到美国，用插件导出json粘贴至从此文件。

      ![13](http://img.imfanqie.top/program/ykt/13.png)

      ![14](http://img.imfanqie.top/program/ykt/14.png)

  * 雨课堂cookie、id获取：

    * 访问雨课堂，打开作业，填写至config.yml或在应用中输入。

    ![15](http://img.imfanqie.top/program/ykt/15.png)

---

* 运行：

  * 主页面命令行：`yktsearch.exe`，不要删除其他文件！

    ![19](http://img.imfanqie.top/program/ykt/19.png)

    ![16](http://img.imfanqie.top/program/ykt/16.png)

  * 运行结束：

    ![17](http://img.imfanqie.top/program/ykt/17.png)

    ![18](http://img.imfanqie.top/program/ykt/18.png)

  * 日志记录（题目文件、BingLog）

    ![21](http://img.imfanqie.top/program/ykt/21.png)

    ![20](http://img.imfanqie.top/program/ykt/20.png)

---

* 报错及其他
  * 报错请参考mainError信息，并仔细阅读readme，遇到问题可以提交issue。
  * 这里只描述了最基本的使用方法和功能，脚本还内置了些其他功能以后会开放，其他使用及功能可以自己探索。

## 使用说明V2.0

* 过渡版本，无说明

## 使用说明V1.0

* 打开雨课堂你要搜的作业（切记，作业搜题用，不要用在考试中，被抓后果自负）

* ctrl+shift+i，或者F12，打开网络工具，刷新页面（尽量跳过控制台，使用控制台会被记录），如图

  ![](http://img.imfanqie.top/program/ykt/1.png)

* 双击左边的名称，拉到最上面，找到show_paper请求，如图

  ![](http://img.imfanqie.top/program/ykt/2.png)

* 右键，复制，复制响应，没有的直接复制右边的全部预览即可，如图

  ![](http://img.imfanqie.top/program/ykt/3.png)

* 打开雨课堂json.txt文件将内容替换上去，如图

  ![](http://img.imfanqie.top/program/ykt/4.png)

* 关闭，双击exe文件，或通过cmd调用即可，完成后会自动打开网页，如图

  ![](http://img.imfanqie.top/program/ykt/5.png)

  ![](http://img.imfanqie.top/program/ykt/6.png)

* 逐个点击链接即可开始愉快的搜题之旅辣！！

## 其他事项

* 不要删除同目录的任何文件！
* **不要改任何东西，需要修改的部分均在config.yml中！**
* 谨慎修改配置文件，推荐使用默认配置。
* 不要将工具用于正规测试，只限在平时作业中使用，否则寄了别找我！
* 注意网页上的提示信息！
* **这里只描述了最基本的使用方法和功能，脚本还内置了些其他功能以后会开放，其他使用及功能可以自己探索。**
* **下个大版本更新GUI界面！**
* 后续可能会更新，看心情，有更新了就发出来了……
* 有大问题提issue，小问题忽略自己查吧。。
* 转载前请注明作者！
