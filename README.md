# wuhexing-666.github.io# 吴贺兴的课程设计个人网站：

通过学习HTML5及CSS3的标准，与他人讨论与交流，利用Gitee/GitHub架Hexo网站，实践RWD课本与WSG课本，实践对界面设计丶信息架构及可用性的基础知识及设计能力做出学习笔记。

##  实践内容

使用Hexo之matery主题模板在Gitee/GitHub上架示范站（多站点设置）

1. [wuhexing-666  GitHub](https://github.com/wuhexing-666/wuhexing-666.github.io)
2. [wuhexing-Gitee](https://gitee.com/wu-hexing/wuhexing666.gitee.io)

  * 程式码[提交记录]((https://github.com/wuhexing-666/wuhexing-666.github.io)
  * 程式码[仓库网路图](https://gitee.com/wu-hexing/projects)

#### 关于我

- [关于我](https://wuhexing-666.github.io/2021/02/26/2021-jiu-dao-liao-huan-shi-xi-wang-zi-ji-nu-li-yi-dian/)

#### 网站设计

- [Hexo网站实现文章分类](https://wuhexing-666.github.io/2021/03/05/hexo-wang-zhan-shi-xian-wen-zhang-fen-lei/)

- [Hexo网站导航栏实现二级标题](https://wuhexing-666.github.io/2021/03/03/hexo-wang-zhan-dao-hang-lan-shi-xian-er-ji-biao-ti/)

- [hexo网站实现代码一键复制识别](https://wuhexing-666.github.io/2021/03/01/hexo-wang-zhan-shi-xian-dai-ma-yi-jian-fu-zhi-shi-bie/)

  

#### 平面设计

- [hexo网站实现雪花飘落效果](https://wuhexing-666.github.io/2021/03/11/hexo-wang-zhan-shi-xian-xue-hua-piao-luo-xiao-guo/)
- [hexo网站添加二次元动漫人物](https://wuhexing-666.github.io/2021/02/26/hexo-wang-zhan-tian-jia-er-ci-yuan-dong-man-ren-wu/)
- [Hexo网站添加鼠标点击爱心效果](https://wuhexing-666.github.io/2021/03/21/hexo-wang-zhan-tian-jia-shu-biao-dian-ji-ai-xin-xiao-guo/)
- [hexo网站添加鼠标点击出现核心价值观](https://wuhexing-666.github.io/2021/03/16/hexo-wang-zhan-tian-jia-shu-biao-dian-ji-chu-xian-he-xin-jie-zhi-guan/)

# 1】添加gittalk评论插件 #

<font color=red size=3>matery</font>主题自带<font color=red size=3>gittalk</font>评论插件，我们只需要开启就可以了。

1.打开[GitHub](https://github.com/settings/applications/new)申请，填写信息：

```javascript
Application name //应用名称，随便填
Homepage URL //填自己的博客地址
Application description //应用描述，随便填
Authorization callback URL //填自己的博客地址
```


![](https://muyiio-1300292673.cos.ap-chongqing.myqcloud.com/%E5%8D%9A%E5%AE%A2/_posts/Hexo-%E4%B8%AA%E4%BA%BA%E5%8D%9A%E5%AE%A2%E4%B9%8B%E5%8D%9A%E5%AE%A2%E5%AE%9E%E7%94%A8%E5%8A%9F%E8%83%BD%E6%B7%BB%E5%8A%A0/04.png)

2.打开<font color=red size=3>themes/_config.yml</font>下修改<font color=red size=3>gitalk</font>那里：

```javascript
gitalk:
  enable: true
  owner: 你的github用户名
  repo: 你的github用户名.github.io
  oauth:
	clientId: 粘贴刚刚注册完显示的字符串
	clientSecret: 粘贴刚刚注册完显示的字符串
  admin: 你的github用户名
```

添加完成。

------



# 2】添加Valine评论系统

**1.进入[LeanCloud](![image-20200417123325676](C:\Users\残废\AppData\Roaming\Typora\typora-user-images\image-20200417123325676.png))官网注册账户，需要实名认证以及邮箱验证**

![](https://muyiio-1300292673.cos.ap-chongqing.myqcloud.com/%E5%8D%9A%E5%AE%A2/_posts/Hexo-%E4%B8%AA%E4%BA%BA%E5%8D%9A%E5%AE%A2%E4%B9%8B%E5%8D%9A%E5%AE%A2%E5%AE%9E%E7%94%A8%E5%8A%9F%E8%83%BD%E6%B7%BB%E5%8A%A0/14.png)



**2.创建应用**



![](https://muyiio-1300292673.cos.ap-chongqing.myqcloud.com/%E5%8D%9A%E5%AE%A2/_posts/Hexo-%E4%B8%AA%E4%BA%BA%E5%8D%9A%E5%AE%A2%E4%B9%8B%E5%8D%9A%E5%AE%A2%E5%AE%9E%E7%94%A8%E5%8A%9F%E8%83%BD%E6%B7%BB%E5%8A%A0/15.png)



**3.进入我们创建的应用，将`AppID`、`AppKey`粘贴到我们的主题配置文件`_config`中**



![](https://muyiio-1300292673.cos.ap-chongqing.myqcloud.com/%E5%8D%9A%E5%AE%A2/_posts/Hexo-%E4%B8%AA%E4%BA%BA%E5%8D%9A%E5%AE%A2%E4%B9%8B%E5%8D%9A%E5%AE%A2%E5%AE%9E%E7%94%A8%E5%8A%9F%E8%83%BD%E6%B7%BB%E5%8A%A0/16.png)



```bash
valine:
  enable: true
  appId: 
  appKey: 
  notify: true      #评论回复提醒
  verify: false     #验证码
  visitor: false    #他人可见
  avatar: 'wavatar' # Gravatar style : mm/identicon/monsterid/wavatar/retro/hide
  pageSize: 10
  placeholder: '如果你没有GitHub账号，还可以在这里评论啦！' # Comment Box placeholder
```



如果没有上面的配置代码，自己添加就可以。

**4.最后更新就可以了，添加邮件通知、云引擎等等可以自己添加**

------



# 3】添加RSS订阅 #

> 简易信息聚合是“Really Simple Syndication”或“Richsite summary”(网站内容摘要)的中文名字。是站点用来和其他站点之间共享内容的一种简易方式。英文缩写为RSS技术。

> RSS是一种信息聚合的技术，是某一站点和其他站点之间共享内容的一种简易信息发布与传递的方式，使得一个网站可以方便的调用其他提供RSS订阅服务的网站内容，从而形成非常高效的信息聚合，让网站发布的内容在更大的范围内传播。他是一种用于共享新闻和其他WEB内容的数据交换规范，也是使用最广泛的一种扩展性标识语言。


**安装：**

1.在本地<font color=red size=3>hexo</font>目录下右键<font color=red size=3>git bash here</font>，输入以下命令：

```javascript
npm install hexo-generator-feed
```

2.安装完成后，打开<font color=red size=3>hexo</font>目录下配置文件的<font color=red size=3>_config.yml</font>，在末尾添加以下代码：

```javascript
# Extensions
## Plugins: http://hexo.io/plugins/
#RSS订阅
plugin:
- hexo-generator-feed
#Feed Atom
feed:
type: atom
path: atom.xml
limit: 20
```

3.最后打开主题配置文件<font color=red size=3>themes/_config.yml</font>，添加以下代码：

```javascript
rss: /atom.xml
```

现在<font color=red size=3>RSS</font>订阅就添加完成。



## 4】添加百度收录SEO

1.安装插件：



```bash
npm install hexo-baidu-url-submit --save
```



2.在根目录 `_config.yml` 文件里加入以下代码：



```bash
baidu_url_submit:
  count: 100                 # 提交最新的多少个链接
  host: git@github.com:wuhexing-666/wuhexing-666.github.io.git # 在百度站长平台中添加的域名
  token:                     # 秘钥
  path: baidu_urls.txt
```



`token`可以在推送接口下面看到：

![](https://muyiio-1300292673.cos.ap-chongqing.myqcloud.com/%E5%8D%9A%E5%AE%A2/_posts/Hexo%E5%8D%9A%E5%AE%A2%E6%8F%90%E4%BA%A4%E7%99%BE%E5%BA%A6%E6%94%B6%E5%BD%95SEO/QQ%E5%9B%BE%E7%89%8720200409003532.png)



3.在根目录的 `_config.yml` 下找到以下配置：



```bash
# URL
## If your site is put in a subdirectory, set url as 'http://yoursite.com/child' and root as '/child/'
url: git@github.com:wuhexing-666/wuhexing-666.github.io.git
root: /
permalink: :year/:month/:day/:title/
```



`url:`后面填写在百度添加的域名



4.在`_config.yml` 加入新的` deployer`

- ```bash
  deploy:
  - type: git
    repository:
      github: git@github.com:wuhexing-666/wuhexing-666.github.io.git
    branch: master
  - type: baidu_url_submitter        #新加的主动推送
  ```

  

5.最后三连上传就可以了,这样显示就是成功

```bash
{"remain":2985,"success":15}           #表示成功15条
INFO  Deploy done: baidu_url_submitter

```



- **自动推送**

1.复制代码

![](https://muyiio-1300292673.cos.ap-chongqing.myqcloud.com/%E5%8D%9A%E5%AE%A2/_posts/Hexo%E5%8D%9A%E5%AE%A2%E6%8F%90%E4%BA%A4%E7%99%BE%E5%BA%A6%E6%94%B6%E5%BD%95SEO/QQ%E5%9B%BE%E7%89%8720200409003536.png)



```javascript
<script>
(function(){
    var bp = document.createElement('script');
    var curProtocol = window.location.protocol.split(':')[0];
    if (curProtocol === 'https') {
        bp.src = 'https://zz.bdstatic.com/linksubmit/push.js';
    }
    else {
        bp.src = 'http://push.zhanzhang.baidu.com/push.js';
    }
    var s = document.getElementsByTagName("script")[0];
    s.parentNode.insertBefore(bp, s);
})();
</script>
```



2.放到`\themes\material-x\layout\_partial\head.ejs`的`<head> `与 `</head> `标签之间。



3.如果主题集成了这个功能，比如 next 主题，在 `themes\next\layout_scripts\` 下有个 `baidu_push.swig` 写入下面代码：

```javascript
{% if theme.baidu_push %}
<script>
(function(){
    var bp = document.createElement('script');
    var curProtocol = window.location.protocol.split(':')[0];
    if (curProtocol === 'https') {
        bp.src = 'https://zz.bdstatic.com/linksubmit/push.js';
    }
    else {
        bp.src = 'http://push.zhanzhang.baidu.com/push.js';
    }
    var s = document.getElementsByTagName("script")[0];
    s.parentNode.insertBefore(bp, s);
})();
</script>
```



然后在文件主题配置文件`_config.yml` 中设置 即可。

```bash
baidu_push: true 
```

5】
