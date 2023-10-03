## 一、介绍
Ayakin是一款基于Typecho默认主题（Typecho Replica Theme）修改而来的轻简风主题，由本人独立开发完成，主题页面主要由浅灰/黑/白色以及主题色构成，采用双栏结构设计，支持不同尺寸屏幕的自适应调整，并可随时切换不同的主题色风格，目前共支持黑、红、蓝、青、绿、金等颜色搭配，不同的主题色组合主要是同色的几种对比度的颜色组成，整体视觉效果简洁、干净、美观。
如果你是第一次使用Ayakin主题，可以参照以下文档配置主题设置。

## 二、文档
### 1.主题色
共分为水墨黑、珊瑚红、深天蓝、水绿青、翡翠绿、烫鎏金，不同的主题色组合主要是同色的几种对比度的颜色组成，选择你喜欢的颜色就行。

### 2.网站图标Url
需要填入一个图标Url，可以直接将图标文件上传到网站目录中后填写图片地址，也可以使用CDN等加速技术，会显示在浏览器标签中。

### 3.导航栏Logo图片Url
同上，会显示在导航栏左侧的标题内容中。

### 4.作者头像地址
同上，会展示在作者信息处及网站首页，留空则根据邮箱自动获取头像，如果自动获取的头像无法显示，请尝试在下方配置项中更换Gravatar头像镜像源地址。

### 5.作者名
会展示在侧边栏的作者信息栏及网站首页，留空则默认显示admin用户昵称。

### 6.作者简介
会展示在侧边栏的作者信息栏及网站首页，留空默认不显示。

### 7.作者标签
多个标签用英文半角逗号“,”分隔，留空则不显示。

### 8.公告
会展示在网站首页最上方，请按照以下规范来填写此项：
该项使用Json数据格式配置，格式为：
```json

[
    {
        "type":"normal",
        "title":"欢迎使用Ayakin！",
        "content":"这是主题默认的公告，你可以在控制台-外观-设置外观-公告中修改或删除它。"
    }
]

```
请注意，在上述格式样例中，最外层需要使用英文半角中括号`[`和`]`包裹，而其中的每一项需要用英文半角大括号`{`和`}`包裹，每一项包含`type`、`title`和`content`三个值，分别对应公告的类型、标题和内容。

公告的类型有`normal（蓝色）`、`success（绿色）`、`warning（橙色）`和`error（红色）`，它们的主题色和样式风格不会随着网站主题色的更换而发生变化。

如果你有多条公告需要显示，可以插入多条由英文半角大括号`{`和`}`包裹的内容，每一条的尾部用英文半角逗号`,`连接，最后一条不需要逗号，类似下面这样：

```json

[
    {
        "type":"normal",
        "title":"欢迎使用Ayakin！",
        "content":"这是主题默认的公告，你可以在控制台-外观-设置外观-公告中修改或删除它。"
    },

    {
        "type":"success",
        "title":"Ayakin启动成功",
        "content":"如果您看到这个公告,表示Ayakin主题已经成功启用."
    }
]

```

### 9.Gravatar头像镜像源地址
Gravatar是一个由WordPress公司提供的头像调用接口，能够根据邮箱号的哈希值获取这个邮箱的头像，因为大陆防火墙的原因，Gravatar头像调用接口经常会出现无法正常访问的现象，Typecho默认的头像来源就是Gravatar接口，所以评论者的头像可能会加载不出来。
为了解决此情况，国内有很多镜像网站，提供了大陆可直接访问的Gravatar头像接口，能够有效避免上述现象的发生，Ayakin主题默认使用的是`cravatar.cn`提供的接口，在大多情况下能够正常加载头像图片，如果你有其他更好、更快的Gravatar接口镜像，可以更改此项。但如果你不知道这个配置项是用来做什么的，或者不了解Gravatar头像接口，请不要更改它。

### 10.文章底部是否显示前后文章导航
关闭后将不会在文章底部显示“上一篇”和“下一篇”链接。

### 11.是否简化页面底部的版权声明
开启后会缩短版权声明长度，格式会由：
```text

© {Year} {SiteName} All Rights Reserved.
Theme Ayakin designed by Lumirant.

```
简化为：
```text

© {Year} {SiteName} Theme by Ayakin.

```
能在小尺寸屏幕的设备上得到更好的视觉体验，进一步简化页面结构。
**请尊重劳动成果，不要擅自修改或删除主题版权标识，感谢你对Ayakin主题的支持。**
**如需商用去除版权声明请联系[开发者][1]，谢谢。**

### 12.置顶文章

能将置顶文章放在网站首页的最上方，需填入指定文章cid，多个文章用英文半角逗号“,”分隔。

### 13.侧边栏显示

自定义网站右边侧边栏显示的内容，默认全选。
注意：屏幕宽度小于992px的设备不会显示侧边栏，这种情况下，该项无效。

### 14.隐藏分类导航

该项会列出网站所有的分类，主题默认会将它们全部显示在导航栏上，如果你不想显示某些分类，请勾选对应的分类名。

### 15.附加导航
会附加在导航栏尾部，请按照以下规范来填写此项。

该项使用Json数据格式配置，格式为：
```json

[
    {
        "name":"Ayakin",
        "link":"https://typecho.lumirant.top",
        "hidden":0
    }
]

```
请注意，在上述格式样例中，最外层需要使用英文半角中括号`[`和`]`包裹，而其中的每一项需要用英文半角大括号`{`和`}`包裹，每一项包含`name`、`link`和`hidden`三个值，分别对应导航的名字、链接和是否隐藏。

名字会显示在导航栏上，点击后会跳转到对应的链接，链接可以是站内的，也可以是站外的。

之所以加入`hidden`这个值，而不是直接选择删除这一项导航来隐藏导航，是考虑到有些导航的配置可能会比较繁琐，或者有多个导航短期内不需要显示，但从长远角度来看却需要一直显示，这个时候就可以改动`hidden`的值，值为0代表不隐藏，值为1代表隐藏，注意这个值是纯数字，不需要加双引号。

如果你有多个导航需要显示，可以插入多条由英文半角大括号`{`和`}`包裹的内容，每一条的尾部用英文半角逗号`,`连接，最后一条不需要逗号，类似下面这样：

```json

[
    {
        "name":"Ayakin",
        "link":"https://typecho.lumirant.top",
        "hidden":0
    },
    {
        "name":"Typecho",
        "link":"https://typecho.org",
        "hidden":0
    }
]

```

### 16.自定义CSS
会注入每个页面的style标签中，优先级除嵌入式样式外最高，可以自定义站内一些样式，直接填入CSS代码即可，无需额外添加`<style>`和`</style>`标签。

### 17.自定义JavaScript
会在每个页面的最后引入，可以自定义站内一些JS规则，直接填入JavaScript代码即可，无需额外添加`<script>`和`</script>`标签。

## 三、下载

Ayain已开源至Github，[点击下载Ayakin主题][2]。

## 四、更新日志

2023-10-3：
- 修复了站名过长时显示不完整的问题 [@Violetmail](https://github.com/Violetmail)
- 页脚添加了备案号显示 [@Violetmail](https://github.com/Violetmail)
- 文章评论关闭时，可自定义底部的文字提示 [@Violetmail](https://github.com/Violetmail)
- 修复了导航栏菜单显示层级错误的问题 [@Lumirant]([https://github.com/Violetmail](https://github.com/lumirant))

2023-10-2：
- 修复了置顶文章为空时渲染出错的问题 [@Lumirant]([https://github.com/Violetmail](https://github.com/lumirant))

## 五、开源协议

Ayakin使用[Apache2.0][3]协议开源，若使用Ayakin主题，你必须遵守Apache2.0协议规定的所有条款，以及声明主题名称及其链接。
请尊重劳动成果，未经主题作者许可，禁止将该主题用于任何商业用途、二次创作和开发及主题移植。
如需商用或去除版权声明请联系[开发者][4]，谢谢。

## 六、交流

您可以加入 QQ 群或当前平台（主题网站、Github仓库、主题文档网站）对主题进行报告错误（Issues）、修复问题(Pull requests)、提高代码质量或提交新功能。

Ayakin主题交流群：751484731

## 七、赞助

如果你觉得主题做的不错，欢迎打赏作者哦
特别提示：合理理财，随缘赞助，请根据自身经济情况决定赞助金额，未成年请不要选择大额赞助~

![赞助](https://github.com/lumirant/Ayakin-Theme/blob/main/img/zanzhu.jfif)


  [1]: https://lumirant.top/
  [2]: https://github.com/lumirant/Ayakin-Theme
  [3]: https://github.com/lumirant/Ayakin-Theme/blob/main/LICENSE
  [4]: https://lumirant.top/
