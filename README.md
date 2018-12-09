## 说明
从网站下载的LeaRun敏捷后台开发框架_6.3.4

这是一个空的后台模板，自带多选项卡效果(重点)

## Ecosystem

| Project | Status | Description |
|---------|--------|-------------|
| python          | 3.5.4 | 在这个版本以及以上都课可以 |
| django                | 2.0.7 | 2.x版本都可以 |

## 遇到的问题

整合花了大量时间,菜单一直没搞出来。后来才发现index.js有问题，修改了一下！
注意：左侧的菜单已经集成到index.html中
如果需要删除无用的，请修改index.js

## 运行方式
 
使用Pycharm直接运行即可，
或者使用命令
`python manage.py runserver`

## 添加新页面
比如,增加通用字典

修改bmt/urls.py,添加url
```python
path('SystemManage/tyzd/', views.tyzd),
```

修改 bmt/backstage/views.py,增加视图函数

```python
def tyzd(request):
    return render(request, "tyzd.html")
```

进入目录 bmt/templates/,新建tyzd.html
```html
<h1>测试一下<h1>
```

修改 bmt/templates/index.html,修改通用字典的href属性
```html
href="/SystemManage/tyzd"><i class="fa fa-book"></i>通用字典
```

最后重启django,刷新页面,重新点击左侧的通用字典,就可以了！

## Bug修复
1. 修复了首页选项卡内容显示问题
2. 修复了无法关闭某些多标签问题
3. 删除多余的静态文件
4. 调整静态目录结构
5. 更新bootstrap-3.3.7以及font-awesome-4.7.0
6. 调整web和api路由,做了路由分发。以及视图函数优化！

## 首页效果如下：

![Image text](https://github.com/tianjinqiujie/bmt/blob/master/效果图.png)

