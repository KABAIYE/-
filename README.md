# <center>你好,这是我的学习笔记</center>

# 一、xpath解析原理
1. 实例化一个etree的对象，且需要将被解析的页面源码数据加载到该对象中
2. 调用etree对象中的xpath方法结合着xpath表达式实现标签的定位和内容的捕获
3. 使用lxml模块
   
## 1.1实例化一个etree对象
 
1. 将本地的html文档中的源码数据加载到etree对象中:
    `etree.parse(filePath)`
2. 可以将从互联网上获取的源码数据加载到该对象中
    `etree.HTML('page_text')`
3. xpath('xpath表达式)

### 1.2xpath表达式
- /: 表示的是从根节点开始定位。表示的是一个层级
- //:表示的是多个层级。可以表示从任意位置开始定位。
- 属性定位: `//div[@class='song'] tag[@attrName="attrValue"]`
- 索引定位: `//div[@class="song"]/p[3]` 索引是从1开始的。
- 取文本：
  - `/text()`获取直系文本 
  - `//text()`获取下属所有文本
- 取属性：
  - /@属性名 

> **爬虫中通用处理中文乱码的解决方案**
> 
> `zhongwen = zhongwen.encode('iso-8859-1').decode( 'gbk')`

> 正则表达式 :
> <https://www.runoob.com/python/python-reg-expressions.html>

######<center> [点一下送地狱火](https://www.bilibili.com/video/BV1GJ411x7h7) </center>

终极目标！！~~不是~~ 
- [ ] 月薪10w+！！！
- [x] 开心
- [x] 好好吃饭









