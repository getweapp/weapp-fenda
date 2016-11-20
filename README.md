# 微信小程序-分答

### 说明：

简单的分答客户端，实现了收听，找人，我的和问答详情页等。特点：

- 基本使用官方推荐的flex来写布局，结合margin和padding能实现大部分的样式要求。
- tabBar的第一个菜单「收听」使用了微信提供的组件scroll-view可滚动视图区域，页面加载后从网络上拉取数据填入视图层同时写入Storage（应该就是html5中的localStorage），滚动到底部时触发更新事件，同时设置标志位防止重复触发。应用官方的加载提示动画。
- 点击某个问题进入问题的详情页，同时导航网址带有该问题的编号，具体数据优先从Storage抓取， 查询不到就请求后台。同样的，点击个人头像或者个人简介bar进入个人详情页。（未完全完成）
- 找人页面的两个榜单均使用template渲染

### 数据接口:

- https://api.getweapp.com/thirdparty/fenda/feeds-init.json
- https://api.getweapp.com/thirdparty/fenda/stamp1206.json

### 目录结构：

- img — 存放项目底部tab图片和实例头像图片
- pages — 存放项目页面相关文件，一共包括feeds,issue,mine,person,search等几个页面
- utils — 存放日期格式化文件

### 开发环境：

微信web开发者工具 v0.10.102800

### 项目截图：

https://www.getweapp.com/project?projectId=583174ecbb2538f8186c7057

### 感谢:

本项目原始版本由davedavehong提供：https://github.com/davedavehong/fenda-mock
