# Github

## 关键字查询
awesome :去此标签类别中查询项目
python tutorial :查询资料，书籍，文档
socket sample :查询对应技术的代码样品

## github三要素

### repository 仓库
仓库是github项目管理存储基本单位
一个仓库存储一个项目，一个用户有多个仓库，分为public,private

### commit 提交
程序员在整个开发周期，有大量的对代码资源的选代和修改，
都可以通过commit的方式进行记录，便于程序员回溯代码，即使这些代码被删除
提交便于使用者观察整个工程的开发流程以及设计流程

### Branch 分支
在仓库中可以包含多个分支，分支才是代码文件的第一存储单位，
默认的仓库主分支为master/main不仅可以管理代码存储，便于多人协作

![pkNv7QA.jpg](https://s21.ax1x.com/2024/06/11/pkNv7QA.jpg)

## 仓库内容
Code，资源存储，代码资源，二进制，项目管理脚本，许可证等等
issues， 使用时遇到的bug或进行提交， 等待反馈
README, 使用markdown语言编写, 工程自述文件，开发进度，，版本更新，使用介绍等等
LICENSE 许可证: GPL2.0,3.0. Apahce 2.0, Mit, 这些许可证，给使用者最大使用权限以及最少的限制

## Git软件，分布式版本控制系统
仓库管理软件，使用git管理私人代码或企业代码
![pkNxkwV.png](https://s21.ax1x.com/2024/06/11/pkNxkwV.png)

## 设备认证
### 1.如何让网站账户和设备绑定，后续完成代码的管理，上传下载
	git init//创建本地仓库
	git config --list//查看git配置文件
	git config --global user.email"邮箱"
	git config --global user.name"用户名"
	ssh-keygen -t rsa -C "注册邮箱" //创建本地密文
#### 去对应目录找密文文件
	rsa. pub 复制密文, 粘贴 settings→SSH key and GPG-> new ssh key->粘贴
	ssh-T git@github.com  //测试关联是否成功
### 2.为目标仓库起别名，定位目标仓库，后续上传
	git remote add orgin "ssh地址" //为ssh仓库地址的创建别名为origin
	git remote remove orgin //删除origin别名

## 本地设备和仓库的交互逻辑
![pkNxKyR.jpg](https://s21.ax1x.com/2024/06/11/pkNxKyR.jpg)

git add .//添加内容
git rm//删除本地文件并删除仓库数据
git restore//恢复被删除，仓库存在

## 代码更新的依赖关系被破坏
本地内容要比云端新，完成更新替换， 但是如果直接修改云端内容，导致本地内容无法再次提交
先拉取git pull云端内容与本地内容合并或操作， 而后再次推即可

git pull --rebase  origin master
git rebase--skip“忽略新版，此时不能上传"
git rebase--abort"忽略旧版，更新后可以上传"
git rebase-continue“版本合并，解决冲突后可以上传"

## 下载开源代码

git clone “https仓库地址”//下载开源项目code源

## 分支Branch

关于分支的相关命令， 创建分支、选择分支、合并分支等等

## Markdown
文本修饰语言，用特殊符号修饰正文效果<br>
 
### 标题修饰符\#

# 标题修饰符（一级标题）
## （二级标题）
### （三级标题）
#### （四级标题）
##### （五级标题）

### 正文
        输入正文，换行用\<br\>标签
### 修饰正文（不同字体）

*哈哈哈*

**哈哈哈**

***哈哈哈***

~~哈哈哈~~

### 分割线
  用\-\-\-表示
---

### 引用效果\>表示
> 666
>> 888
>>> 999
>>>> 1314
符号数对应几级引用

### 列表修饰符
#### 无需列表 \*
* 无语
  * 张雪怡
    * 冯笑
* 啦啦啦
  * 哈哈哈
  * 呵呵呵

#### 有序列表 1.
1. 物理
   1. 换行
   2. 更改
   3. 天天
   4. 问题
2. 链路
   1. 换行
   2. 看看

####混合列表
1. 一
   * 二
     2. 三

#### 表格
名称|技能|排行
--|:--:|--:
蝙蝠侠|有钱|1
冯笑|无敌|6
詹妮弗|闪光灯|3

#### 代码片段

```c
        printf("but");
```

```cpp
        cout<<"but"<<endl;
```

```python
        我不会python
```

```bash
        pwd
        ls -l























