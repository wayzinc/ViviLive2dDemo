> live2d 学习和测试demo

### 前言
>ive2d 是一项类3D的2D渲染技术，是可以栩栩如生的表现出人物表情和情感的全新动画技术，使用范围广泛，可以用于游戏、网页制作等，在bilibili等视频网站可以搜到大神们制作模型的教程。现在部分主播的虚拟形象也是用Live2d技术来实现的，这些虚拟形象主播统称为VTuber。

本文章只介绍在网页中加载Live2d的方法，比如在我的博客右下角，有一只小黑猫，就是用Live2d加载出来的模型；早期我在网站中分别实现过猫和血小板的模型加载，效果如下：
(模型来源于互联网)
![](/media/202407/2024-07-23_151124_1676430.235552547917246.png)

### 预览和仓库
>__预览地址__
>__仓库地址__
```
git clone https://github.com/wayzinc/ViviLive2dDemo
```

### 具体用法
> __核心代码：__
引入js依赖，用load方法加载模型json文件即可
```
<canvas id="live2d" width="300" height="300"></canvas>
<script src="js/live2d.min.js"></script>
<script>
    loadlive2d("live2d", 'model/22/model.default.json');
</script>
```

>核心代码真的就这么简单一句话，就能实现加载模型，至于剩下的功能，例如长按跟随鼠标拖动，右键点击穿透，文字对话和换装等功能，都是需要另外写js来实现的，这个js只是最基本的加载模型，刚好符合我的需求。

> __更换模型：__
如果需要替换其他模型，参考具体目录如下，替换模型加载地址即可
```
# 22娘(B站)
model/22/model.default.json
# 33娘(B站)
model/33/model.default.json
# 羊栖菜(黑猫)
model/hijiki/hijiki.model.json
# 山药泥(白猫)
model/tororo/tororo.model.json
# 小埋
model/xiaomai/xiaomai.model.json
# 碗中小年糕
model/wanko/wanko.model.json
# 血小板
model/platelet-3/kesyoban.model.json
```

### 参考资源
>说明：本项目是学习参考github上的项目作精简提取，只供学习用途。

> __imuncle__ 地址：https://github.com/imuncle/live2d
> __zzzmhcn__ 地址：https://github.com/zzzmhcn/live2dDemo