<div align="center">

![展示](README/miniprogramming_log.png) 
    <h1> 桂院导航小程序 </h1>

[![test](https://gitee.com/talmudmaster/GLU-Campus-Guide/badge/star.svg?theme=dark)]()
[![test](https://gitee.com/talmudmaster/GLU-Campus-Guide/badge/fork.svg?theme=dark)]()
[![test](https://img.shields.io/badge/platform-微信小程序-green)]()

首款同时实现云开发和静态项目的校园导航小程序  
提供校园导航和校园信息服务，具有出色的用户体验

***B站讲解视频：先鸽着***  
***CSDN开发笔记：[桂院导航小程序开发日记](https://blog.csdn.net/weixin_45940369/article/details/129279263)***

☑️地图选点与搜索  ☑️地图路径规划  ☑️校园信息展示  ☑️在线管理地点数据

</div>

---

## 📖介绍
  
桂院导航小程序（毕设）  

桂院导航是一款以地图为载体，提供**桂林学院**校园地点的位置信息、导航、校园信息介绍的小程序。  
旨在解决传统地图的校园标识不到位、地图形式低效单一、信息设计不够好等问题，为来桂院的新生和游客提供更加完美的出行体验。

<div align=center>

**仅需修改地图配置文件和云端数据，即可适配任意校园的小程序个性化地图定制。**

原生小程序 + 腾讯位置服务路线规划插件 + 云开发能力

项目开源，持续维护，欢迎 [反馈](https://github.com/talmudmaster/GLU-Guide/issues)、[PR](https://github.com/talmudmaster/GLU-Guide/pulls) 和 Star⭐️！

</div>  

---
## 🤩预览

![展示](README/show_1.png)  

![展示](README/show_2.png)

![小程序信息](README/miniprogramming_card.png)  
答辩后若无学校经费支持改为发行静态版本（云开发费钱）  

---
## ⚡️ 功能

- ✅ 校园地点分类动态展示
- ✅ 地点选择与搜索
- ✅ 路线规划
- ✅ 校园信息
- ✅ 可跳转至学校官网/官微/官方小程序
- ✅ 在线管理地点数据
- ✅ 在线上传修改手绘地图、封面图片、轮播图及视频

---
## 📝小程序使用说明

![使用说明](README/instruction.png)

---
## 🗄软件架构

伪流程图
![云开发伪流程图](README/liuchengtu.png)


---
## 🔬安装教程

1.  自行填写utils.js中的[腾讯位置服务API](https://lbs.qq.com/)和[和风天气API](https://dev.qweather.com/)的key（没有就去申请）
2.  部分图片引用自免费图床-[CDN加速图床](https://cdnjson.com/)（自行替换）
3.  地图边界和自定义图层（自己绘制的地图）边界坐标都写死了，可自行修改或改为云开发管理方式。
4.  静态版本数据存储在utils.js中，图片（除图标）均引用自图床，视频引用自己的Gitee Page中的视频（没想到其他好方法）
5.  云开发版本map.js自行修改getdefaultsite(),静态版本map.js自行修改default_category变量,自定义默认位置
6.  云开发版本需开通云开发功能，建立对应的集合，然后上传数据即可（会提供案例数据json文件）
7.  admin.json自行添加管理员的openid（添加管理员功能暂时没做）
8.  如有需要，自行更换图片、链接或修改代码功能
9.  若图片过大加载较慢，可压缩图片再上传 [图片压缩网站](http://jisu123.cn/)

---
## ❤致谢

非常感谢以下的小程序开发者和B站up，以及教会、锻炼我PS能力的校红会小伙伴  
让我学到了很多，得以把小程序做到今天这样完整
![致谢](README/zhixie_all.png)

---
## 🎈远期构想
外校或本校未来学校扩建，那么现在的小程序是需要修改的，如果想在此基础上开发，需注意：   
- 新地图可以在我的地图上用PS继续绘制（我就是在学校早期规划图基础上用PS修改得来的），或者自己重新绘制（考虑要不要出0基础画简单地图的教程）。
- **更好的路线导航方式**是自己绘制“图”，并使用最短路径算法实现（下面给出案例图和讲解）。     
![构建图](README/build_map.png)  
图中红色点为地点，蓝色点为道路点。蓝色线段即为点之间的关系（一个道路点能够到达其他的什么点）。就可以模拟出“图”以及其所有点之间的关系。点与点之间“路”的长度可以通过公式计算出（**注意地球是球体-曲面，经纬度计算距离的公式可以百度**）。有了点之间的关系以及“路”（边）的长度，可以通过最短路径算法计算出最短路经过的所有点并显示到地图上。

---
## 🧾参考资料

- [微信官方文档 · 小程序](https://developers.weixin.qq.com/miniprogram/dev/framework/)
- [莞香广科 · 校园导览](https://gitee.com/hm_anwei/school-map)
- [信科校园导览小程序](https://gitee.com/talmudmaster/GIIT-campus-guide)
- [地大校园导航](https://gitee.com/min_yue/CUG_Campus-navigation)

---
## 📒开源许可证
 
请认真阅读并遵守以下开源协议

[MulanPSL-2.0](https://gitee.com/talmudmaster/GLU-Campus-Guide/blob/master/LICENSE)

欢迎 pull request and star

允许任何人对该项目进行变动

同时欢迎各位开发者参与到该项目(在软件声明与致谢页面加入参与贡献者名称)

禁止用于商业和非法目的，使用代码请标明出处或有所声明
