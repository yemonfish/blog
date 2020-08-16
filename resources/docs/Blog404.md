# Blog404

## 简介

前后端分离型个人博客系统，有前台展示页面和后台管理系统，可多账号协同管理。集摄影、电影、音乐、学习笔记、日记等模块为一体，可用于知识管理、影像收藏、作品展示、生活记录。解决LeetCode、Instagram、LOFTER、豆瓣电影、豆瓣音乐、豆瓣读书、微博等平台功能分散，本地主机存储无法按需展示的问题，旨在打造一站式资料收藏陈列系统。

### 效果图

### 在线Demo

在线演示地址：/*          */

测试用管理员账号密码：/*          */

## 版本与技术栈

### 前端

- Vue+ElementUI+Axios实现的前台展示页面，各模块色系独立，样式统一。

    项目根目录：Blog404/Front/Blog404-Client-ElementUI

    开发笔记详见：Blog404/resources/docs/前端 - 前台博客页面

- Vue+Axios实现的前台展示页面，各模块样式独立。

    项目根目录：Blog404/Front/Blog404-Client-Independent

    开发笔记详见：Blog404/resources/docs/前端 - 后台管理系统

### 后端

- Spring Boot+MyBatis Plus+Redis+RocketMQ+Shiro实现的后台管理系统。

    项目根目录：Blog404/End/Blog404-SpringBoot

    开发笔记详见：Blog404/resources/docs/后端 - Spring Boot版

- Spring Cloud+Oracle+Redis+Kafka+Shiro实现的后台管理系统，微服务型。

    项目根目录：Blog404/End/Blog404-SpringCloud

    开发笔记详见：Blog404/resources/docs/后端 - Spring Cloud版

## 运行

### 前端

在前端项目根目录下运行Git Bash，执行下列指令，浏览器将自动打开项目。

```vue
cnpm install
npm run dev
```

- 运行端口号在config/index.js文件内修改。

- 后端交互URL在src/utils/request.js文件内修改。

### 后端

- Spring Boot+MyBatis Plus+Redis+RocketMQ+Shiro实现的后台管理系统。

    项目根目录：Blog404/End/Blog404-SpringBoot

    - 启动端口号在/*          */文件内修改

    - 修改数据库连接

        /*          */文件内修改

    - 启动Redis

        ```
        
        ```

    - 启动RocketMQ

        ```
        
        ```

    - 启动Spring Boot启动类

        /*          */

- Spring Cloud+Oracle+Redis+Kafka+Shiro实现的后台管理系统，微服务型。

    项目根目录：Blog404/End/Blog404-SpringCloud

    - 启动端口号分别在各模块的/*          */文件内修改

    - 修改数据库连接

        /*          */文件内修改

    - 启动Redis

        ```
        
        ```

    - 启动Kafka

        ```
        
        ```

    - 启动各模块启动类

        /*          */

### 数据库

数据库文件目录：Blog404/resources/databases

数据库中执行.sql文件，导入数据库。

含原始.xlsx文件，便于修改内容。修改后可在Navicat中将.xlsx导入成数据记录。

## 模块与功能

### 前台展示页面

模块：HOME / CODE / PHOTOGRAPH / MOVIE / MUSIC / READING / DAILY / CONTACT

#### HOME

首页。

- 支持自动播放背景音乐，可暂停。/*     音量调节已隐藏待开放，待实现切歌     */
- 有头部导航栏、右上角估计迷你可全屏展开网格导航栏。
- 背景图片走马灯切换，hover时显示切换键。
- banner位置有鼠标粒子特效，不遮挡信息。
- 鼠标点击有爱心上浮特效。

#### CODE

模块：Java / Go / Front-End / Algorithm

代码、题解、笔记。

- 支持文章分页显示，默认按后台管理系统设置的优先级排序，可按时间顺序排序。
- 支持关键词搜索、按标签分类。
- 详情页支持代码高亮显示。
- 详情页可插入图片，点击图片可全屏显示。

- 已登录用户可进行文章收藏，留言讨论。

#### PHOTOGRAPH

模块：Favorite / Album / Timeline / Photographer

摄影作品展示，相册，摄影时间线记录，摄影师及其摄影集收藏。

##### Favorite

- 摄影作品展示，从相册中获取标为待展示的图片，按后台管理系统设置的优先级排序。默认显示全部类型，支持按人文、人像、风光等类型分类。

##### Album

- 图片按相册分类，相册列表按后台管理系统设置的优先级排序，可按创建时间顺序排序。

- 相册详情页含图片列表+相册文字描述，hover可预览大图。
- 图片详情含图片全屏显示+图片文字描述+图片参数信息，可走马灯切换。

##### Timeline

- 按原创图片发布批次归档，按发布时间线倒序。
- 单条发布详情含图片列表+该条动态文字描述，hover可预览大图。
- 点击图片可全屏显示，含图片文字描述+图片参数信息，可走马灯切换。

##### Photographer

- 默认显示所有收藏的摄影师，按后台管理系统设置的优先级排序。
- 支持关键词搜索。
- 世界地图中各国按该国籍摄影师数量呈现相应深浅的背景色。
- 世界地图hover可显示已收藏的该国籍的摄影师名字列表。
- 点击世界地图显示相应国籍的摄影师列表。
- 点击摄影师进入其详情页，含图片+信息介绍，下滑出现其摄影集列表。
- 点击摄影集进入其详情页，含摄影集信息介绍+摄影作品列表，按后台管理系统设置的优先级排序。
- 点击图片可全屏显示，含图片文字描述+图片参数信息，可走马灯切换。

#### MOVIE

模块：Director / List

导演及其执导影片收藏，电影海报、剧照收藏，影评记录。影片包括电影、纪录片、mv、广告、真人秀等各种形式的影像。

##### Director

- 默认显示所有收藏的导演，按后台管理系统设置的评分排序。
- 支持关键词搜索。
- 世界地图中各国按该国籍导演数量呈现相应深浅的背景色。
- 世界地图hover可显示已收藏的该国籍的导演名字列表。
- 点击世界地图显示相应国籍的导演列表。
- 点击导演进入其详情页，含图片+信息介绍，点击more进入该导演图片列表，点击图片可全屏显示，可走马灯切换。下滑出现其执导影片列表，按后台管理系统设置的评分排序，可按上映时间排序。
- 点击影片进入其详情页，含影片信息介绍+影评+剧照缩略图+珍藏镜头，可从该影片已上传的海报或剧照中选择一些添加到影评内。
- 点击剧照more可浏览该影片所有的海报+剧照，左上角可切换显示海报或剧照。/*     v-show     */
- 点击图片可全屏显示，含图片文字描述，可走马灯切换。

##### List

- 默认显示所有收藏的影片，可切换显示已看或想看，默认为已看。已看按后台管理系统设置的评分排序，未看按后台管理系统设置的优先级排序。
- 世界地图中各国按该制片地的影片数量呈现相应深浅的背景色。
- 世界地图hover可显示已收藏的该国制片的影片名字列表。
- 点击世界地图显示相应制片国的影片列表。
- 可按发行时间、类型等标签进行分类，支持关键词搜索。
- 点击影片进入其详情页，含影片信息介绍+影评+剧照缩略图+珍藏镜头，可从该影片已上传的海报或剧照中选择一些添加到影评内。
- 点击剧照more可浏览该影片所有的海报+剧照，左上角可切换显示海报或剧照。/*     v-show     */
- 点击图片可全屏显示，含图片文字描述，可走马灯切换。

#### MUSIC

模块：Artist / PlayList

歌手、专辑、单曲、专辑收藏。

##### Artist

- 默认显示所有收藏的歌手，按后台管理系统设置的优先级排序。
- 支持关键词搜索。
- 世界地图中各国按该国籍歌手数量呈现相应深浅的背景色。
- 世界地图hover可显示已收藏的该国籍的歌手名字列表。
- 点击世界地图显示相应国籍的歌手列表。
- 点击歌手进入其详情页，含图片+信息介绍，点击more进入该歌手图片列表，点击图片可全屏显示，可走马灯切换。下滑出现其专辑列表，按后台管理系统设置的评分排序，可按发行日期排序。
- 点击专辑进入其详情页，含专辑信息介绍+歌曲列表+专辑封面。点击封面可全屏显示。
- 点击音乐进入播放页面，可播放mv，有专辑封面旋转唱片，点击则切换为滚动歌词，有相应控制面板。

##### PlayList

- 默认显示所有创建的歌单，按后台管理系统设置的优先级排序。

- 支持关键词搜索。

- 点击歌单进入其详情页，含歌单信息介绍+歌曲列表+歌单封面。点击封面可全屏显示。
- 点击音乐进入播放页面，可播放mv，有专辑封面旋转唱片，点击则切换为滚动歌词，有相应控制面板。

#### READING

模块：Note / Author

作家收藏，书评、摘录、笔记。

##### Note

- 支持关键词搜索、按标签分类。

- 默认显示所有笔记，含标题+摘要。默认按后台管理系统设置的优先级排序，可按时间顺序排序。
- 详情页支持重点词或段落的高亮和注释。可插入图片，点击图片可全屏显示。

##### Author

- 默认显示所有收藏的作家，按后台管理系统设置的优先级排序。
- 支持关键词搜索。
- 世界地图中各国按该国籍作家数量呈现相应深浅的背景色。
- 世界地图hover可显示已收藏的该国籍的作家名字列表。
- 点击世界地图显示相应国籍的作家列表。
- 点击作家进入其详情页，含图片+信息介绍，点击more进入该作家图片列表，点击图片可全屏显示，可走马灯切换。下滑出现其书籍列表，按后台管理系统设置的评分排序，可按出版日期排序。
- 点击书籍进入其详情页，含书籍信息介绍+摘录+书评。

##### Bookcase

- 默认显示所有收藏的书籍，按后台管理系统设置的评分排序。

- 支持关键词搜索，支持按类型、关键词分类。

- 点击书籍进入其详情页，含书籍信息介绍+摘录+书评。

#### DAILY

日记、随笔、猫咪成长记录、旅行记录、旅行地点收藏、网站收藏

模块：Journal / Kittens / Travel / Collection

##### Journal

- 默认显示所有日记，不折叠，按发布时间倒序。
- 可插入图片，点击图片可全屏显示。

##### Kittens

- 猫咪日龄、体重、食量随日期变化的折线图。共3*n条折线，默认显示所有猫咪的体重折线。点击折线可增加显示或取消显示对应的数据，纵坐标可自适应。
- 默认显示所有的成长图文记录，按发布时间倒序。点击猫咪头像可切换到该猫咪的成长图文记录列表。
- 支持发布视频。

##### Travel

- 默认显示所有收藏的旅行地点，按后台管理系统设置的优先级排序。
- 支持关键词搜索，按人文、建筑、地质、自然风光等标签分类。
- 地图中各地区按该地区已收藏的子地区数量呈现相应深浅的背景色。
- 地图hover可显示该地区已收藏的子地区名字列表。
- 点击地图可进入下一级子地区，同时显示该子地区的旅行地点列表。
- 点击旅行地点进入其图文详情页。点击图片可全屏显示。

##### Collection

- 一些常用网站的收藏，默认按后台管理系统设置的推荐程度排序。
- 点击后在新标签打开。

#### CONTACT

联系方式。

- Email，点击后自动打开邮件发送页面。

- Wechat，hover时在旁边显示二维码。
- GitHub、Instagram、Sina，点击后在新标签打开。
- 游客或已登录用户可发送留言或反馈信息。表单包含昵称、手机号码、邮箱、内容。

#### User

- 游客注册
- 账号绑定微信
- 用户登录，支持微信登录。
- 查看个人主页
- 修改个人资料
- 查看站内消息，包含私信。

### 后台管理系统

#### HOME

- 登录。拥有多个博客管理权限的用户需选择其一进入后台管理系统。
- 退出
- 查看个人信息，包括头像、昵称、简介、Email、GitHub、Wechat、Instagram、Sina、拥有权限的博客列表等。
- 修改个人信息
- 取消对某非自身博客的管理

#### CONFIG

- 博客信息设置：Title、域名。
- 博客主题设置：各模块Menu图、Cover图、Banner图、Background图、背景音乐选择。

#### STATISTICS

- 用户数量、用户增长量统计。（仅超级管理员、网站管理员可见）
- 所有用户访客总量统计（仅超级管理员、网站管理员可见）
- 各用户访客量统计，默认按数量倒序，可切换为正序。（仅超级管理员、网站管理员可见）
- 所有用户博客文章被收藏总量统计（仅超级管理员、网站管理员可见）
- 各用户博客文章被收藏统计，默认按数量倒序，可切换为正序。（仅超级管理员、网站管理员可见）

- 当前博客访客量统计
- 当前博客文章被收藏量统计

#### MESSAGE

- 查看收到的反馈信息列表，默认显示全部信息，可切换为未回复列表或已回复列表。
- 消息提醒列表，含被收藏提醒、被评论提醒、反馈提醒、反馈被回复提醒。默认显示未读的全部类型消息，可选择相应类型的提醒列表，可切换为已读列表。
- 处理反馈信息，可选择回复方式：短信、邮箱、站内私信。站内私信只可针对已注册用户的反馈信息，回复内容将发送到对方后台管理系统的MESSAGE模块的已发送的反馈信息列表的反馈详情页的被回复部分，同时在对方后台管理系统的MESSAGE模块的消息提醒列表处添加被回复提醒。
- 删除反馈信息
- 查看文章评论列表，默认显示全部评论，可切换为未回复列表或已回复列表。
- 回复评论

#### 角色与权限

- 超级管理员

    同为用户。可凭账号密码登录后台管理系统。拥有该网站顶级权限，管理所有网站管理员、用户、博客，可添加该网站的普通管理员，为其分配额外权限。

- 网站管理员

    拥有该网站次级权限，除了网站管理员拥有的基本权限，还拥有超级管理员额外分配的权限。管理用户、博客。其下有众多二级角色。

- 用户

    用户即博主，注册成功后拥有个人博客。可凭账号密码登录后台管理系统，管理自己的博客。拥有自己博客的顶级权限，可在后台添加其他用户为博客管理员，协同管理该博客，可为其分配额外权限。可与其他博客进行互动，如收藏内容、留言、提交反馈、接收站内消息与私信，留言会显示在客户端页面，反馈只显示在接收方的后台管理系统。

- 博客管理员

    同为用户，拥有自己的博客，同时受邀成为某博客的博客管理员。可凭账号密码登录后台管理系统，选择进入管理拥有权限的博客。其下有众多二级角色。

- 游客

    可浏览博客、提交反馈，反馈只显示在接收方的后台管理系统。

##### User

- 查看用户列表（仅超级管理员、网站管理员可见）
- 查看用户详情，包含登录时间、登录次数、在线时长、操作记录。（仅超级管理员、网站管理员可见）
- 编辑用户状态，如设置禁言、冻结账号。（仅超级管理员、网站管理员可见）

##### Admin

- 查看权限列表。对于网站管理员才可拥有的权限，仅超级管理员、网站管理员可见。
- 添加权限，仅超级管理员可见。
- 修改权限，仅超级管理员可见。
- 删除权限，仅超级管理员可见。
- 查看角色列表
- 添加角色，分配权限。仅博主可见。对于添加网站管理员的二级角色，仅超级管理员可见。
- 修改角色信息、所拥有的权限。仅博主可见。对于修改网站管理员的二级角色，仅超级管理员可见。
- 删除角色。仅博主可见。对于修改网站管理员的二级角色，仅超级管理员可见。
- 查看管理员列表。仅博主可见。对于网站管理员列表，仅超级管理员可见。
- 查看管理员操作日志。仅博主可见。对于网站管理员操作日志，仅超级管理员可见。
- 添加管理员，指定角色，可分配给该管理员额外权限。仅博主可见。对于添加网站管理员，仅超级管理员可见。
- 修改管理员权限。仅博主可见。对于修改网站管理员权限，仅超级管理员可见。
- 删除管理员。仅博主可见。对于删除网站管理员，仅超级管理员可见。

#### CODE

- 查看文章列表
- 查看文章信息，包含分类、标签、摘要、详情、评论列表、被收藏数量。
- 查看分类列表
- 查看标签列表
- 查看评论列表
- 新增文章，并设置分类、标签、摘要、详情。
- 新增分类
- 新增标签
- 修改分类
- 修改标签
- 修改文章，可修改分类、标签、摘要、详情。
- 删除文章
- 删除分类
- 删除标签
- 删除评论

#### PHOTOGRAPH

- 创建相册。
- 发布时间线图文记录，为已添加的图片分别添加文字描述、参数信息，并指定所属相册，可批量处理。
- 时间线发布成功后，图片异步上传到指定相册。
- 从相册中选取展示作品，并排序。
- 添加摄影师，填写信息，选择国籍，上传照片，可选择其一作为封面。
- 添加摄影集，并添加文字介绍，选择归属摄影师。
- 添加摄影集作品，并分别设置描述信息。

#### MOVIE

- 查看标签列表
- 查看导演列表
- 查看影片列表
- 创建标签
- 添加电影
- 添加导演

#### MUSIC

- 创建标签
- 创建歌单
- 添加歌手

#### READING

- 创建标签
- 添加书籍
- 添加作家

#### DAILY

- 

## 数据库设计

## 接口设计

### CONFIG

- 获取blog信息

    client/home/getBloggerInfoByDomain

    GET

    request：domain

    response：bloggerId , avatar , nickname , introduce 

    desc：根据访问的域名查询user表，获取博主信息。将bloggerId存入全局，待后序访问用。

- 获取blog主题

    client/home/getThemeByDomain

    GET

    request：domain

    response：theme_coverList , theme_menu_code , theme_menu_photograph , theme_menu_movie , theme_menu_music , theme_menu_reading , theme_menu_daily , theme_menu_contact , theme_banner_code , theme_banner_photograph , theme_banner_movie , theme_banner_music , theme_banner_reading , theme_banner_daily , theme_banner_contact , theme_background_code , theme_background_photograph , theme_background_movie , theme_background_music , theme_background_reading , theme_background_daily , theme_background_contact

    desc：根据访问的域名查询theme表，获取博客主题图片地址，存入全局，待后序访问用。

### USER

### ADMIN

- 新增权限
- 修改权限
- 删除权限
- 新增管理员
- 修改管理员信息
- 删除管理员

### CONTACT

- 获取blogger联系信息

    client/contact/getContactByBloggerId

    GET

    request：bloggerId

    response：email , github , wechat , instagram , sina

    desc：取出存入全局的bloggerId，查询user表，获取其联系信息。

    

    



 




