# Panda-OJ-Go
pandaOJ-go的重塑版，重新整理了业务逻辑，构建新的项目结构
## 简介
出于好奇心和兴趣，以力扣和洛谷两款在线判题平台产品为参考进行研究和分析。最终决定动手实现这两款产品的核心功能部分（即将用户提交的代码进行在线编译和执行，然后比较结果）。
## 项目架构图
![项目架构图](/imgs/pa.png)
## 项目结构
```
panda-oj
-- client
-- producer
-- comsumer
-- sanbox_image
```
## 项目结构分析
### client
- 前端代码存放处
- 基于vue和原生h5、css方式实现的用户界面，主要通过给AI提供prompt引导AI生成整体界面，后手动添加/修改部分代码去完成界面的开发工作
### producer
- 项目架构图中producer部分的代码存放处
- 提供用户注册、登录、题目列表检索、提交代码、获取判题结果等功能
### comsumer
- 项目架构图中consumer部分的代码存放处
- 主要提供用户代码在线编译、执行和结果比较等核心功能
### sanbox_image
- 自制沙箱镜像代码存放处
- 目的是提供安全环境执行用户所提交的代码
## 主要技术栈
- golang、gin、gorm、jwt
- kafka、redis、mysql、minio、docker、websocket

## 运行效果图
- 题目列表
![题目列表界面](/imgs/p_list.png)
- 题目详情示例
![hello,world](/imgs/p_hello.png)
![sanjiao](/imgs/p_sj.png)
- 进行代码编写并提交
![coding](/imgs/ans.png)
- 提交后进行判题等待
![judging](/imgs/judging.png)
- 得到结果（和两大平台一样AC表示答案正确,同时显示代码运行时间和占用内存）
![result](/imgs/res.png)

## 后语
目前只是实现OJ的核心功能，还有很大的发挥空间去丰富内容和改善代码，留着以后有空闲时间再慢慢完善吧，实在是有太多有趣的东西需要花费时间精力去钻研和学习了。不过，实现核心功能部分也算是完成初衷了。研究、学习、设计、实现的过程真的很有意思，希望未来可以在钻研过程中变得越来越渊博吧
