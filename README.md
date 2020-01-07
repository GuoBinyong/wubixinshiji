[袖珍简化字拼音]: https://github.com/rime/rime-pinyin-simp
[東風破]: https://github.com/rime/plum
[仓库地址]: https://github.com/GuoBinyong/wubixinshiji
[issues]: https://github.com/GuoBinyong/wubixinshiji/issues
[Rime输入法]: https://rime.im
[百度云盘]: https://pan.baidu.com/s/1bUdEAz7W8hC_imi66WVnaQ
[Rime定制指南]: https://github.com/rime/home/wiki/CustomizationGuide




目录
=================
<!-- TOC -->

- [1. 输入方案介绍](#1-输入方案介绍)
    - [1.1. 新世纪五笔](#11-新世纪五笔)
    - [1.2. 新世纪五笔·拼音](#12-新世纪五笔·拼音)
    - [1.3. 新世纪五笔·简入繁出](#13-新世纪五笔·简入繁出)
- [2. 依赖](#2-依赖)
- [3. 安装与配置](#3-安装与配置)
    - [3.1. 安装](#31-安装)
        - [3.1.1. 方式1：東風破](#311-方式1東風破)
        - [3.1.2. 方式2：手动安装](#312-方式2手动安装)
    - [3.2. 配置](#32-配置)
    - [3.3. 部署](#33-部署)
- [4. 附：Rime输入法简介](#4-附rime输入法简介)
- [5. 作者信息](#5-作者信息)

<!-- /TOC -->


---------------


内容
===================


> 方案下载地址
> - [GitHub仓库地址][仓库地址] : <https://github.com/GuoBinyong/wubixinshiji>
> - [百度云盘][] : 链接：<https://pan.baidu.com/s/1bUdEAz7W8hC_imi66WVnaQ> 提取码：v234


# 1. 输入方案介绍
这是一套[Rime输入法][]的[新世纪五笔输入方案集][仓库地址]，并且支持自动匹配 emoji 表情，该方案集里有以下Rime输入方案：


## 1.1. 新世纪五笔
**方案ID:** `wubixinshiji`  
**方案文件:** `wubixinshiji.schema.yaml`  
以五笔输入为主，通过输入`z`字母临时切换到拼音输入方案；支持自动匹配 emoji 表情；


## 1.2. 新世纪五笔·拼音
**方案ID:** `wubixinshiji_pinyin`  
**方案文件:** `wubixinshiji_pinyin.schema.yaml`  
可以直接输入五笔 或 拼音，会自动识别五笔 和 拼音；支持自动匹配 emoji 表情；

## 1.3. 新世纪五笔·简入繁出
**方案ID:** `wubixinshiji_trad`   
**方案文件:** `wubixinshiji_trad.schema.yaml`  
通过输入简体五笔的编码，来输出相应的繁体字；支持自动匹配 emoji 表情；




# 2. 依赖

拼音反查、五笔拼音混合输入功能依赖于以下输入方案：  
  - [袖珍简化字拼音][] ℞ **`pinyin-simp`**


# 3. 安装与配置

## 3.1. 安装
### 3.1.1. 方式1：東風破
[東風破][]安裝命令：`bash rime-install GuoBinyong/wubixinshiji pinyin-simp`



### 3.1.2. 方式2：手动安装
1. 安装新世纪五笔方案集
   将以下文件或目录拷贝到Rime输入法的用户配置目录中:  
   
   - [x] `wubixinshiji.dict.yaml` : 必选；五笔码表文件
   - [x] `opencc` : 必选；如果用户配置目录下已经有该目录，则把该目录的所有文件拷贝到用户配置目录下    `opencc` 目录中；
   - [ ] `wubixinshiji.schema.yaml` : 可选； 新世纪五笔 输入方案
   - [ ] `wubixinshiji_pinyin.schema.yaml` : 可选； 新世纪五笔·拼音 输入方案
   - [ ] `wubixinshiji_trad.schema.yaml` : 可选； 新世纪五笔·简入繁出 输入方案

2. 安装依赖方案 _袖珍简化字拼音_；（如果已经安装，请忽略此步）
   由于拼音反查、五笔拼音混合输入功能依赖于 _袖珍简化字拼音_ ，所以，如果您还没有安装  _袖珍简化字拼音_，那你同样需要安装 _袖珍简化字拼音_ ， _袖珍简化字拼音_ 的下载地址如下：
   - [GitHub仓库地址][袖珍简化字拼音]
   - [百度云盘][] : 链接：<https://pan.baidu.com/s/1bUdEAz7W8hC_imi66WVnaQ> 提取码：v234
   
   将以下文件或目录拷贝到Rime输入法的用户配置目录中:  
   - [x] `pinyin_simp.dict.yaml` : 必选；袖珍简化字拼音码表文件
   - [x] `pinyin_simp.schema.yaml` : 必选； 袖珍简化字拼音 输入方案



## 3.2. 配置
输入方案安装好后，还需要把需要用的输入方案加入方案选单，详细的配置方法，请参考[Rime定制指南][]，本文只简单教授其：

在用户配置目录中
- 如果没有 `default.custom.yaml` 文件，则把百度云盘中的 `default.custom.yaml` 直接拷贝到 用户配置目录中；

- 如果有 `default.custom.yaml` 文件，则在该文件中的 `schema_list:` 下添加以下配置
   ```
       - schema: wubixinshiji    # 新世纪五笔
       - schema: wubixinshiji_pinyin    # 新世纪五笔·拼音
       - schema: wubixinshiji_trad    # 新世纪五笔·简入繁出
   ```

**注意事项：**
- 添加时，每行前面的空格要和之前的保持一致；
- 只添加你需要的方案，不需要的方案可以不用添加，或者在不需要的方案选单那行的行首添加个 `#`，如下：
  ```
  #    - schema: wubixinshiji_trad    # 新世纪五笔·简入繁出
  ```


## 3.3. 部署
点击 **部署** 按钮： Rime输入法的特点是，当你完成配置后，需要点击 **部署** 按钮，才能让输入法执行你的配置.




# 4. 附：Rime输入法简介
**[Rime输入法][]**可谓**神级输入法**，利用它，你完全可以通过配置文件来达到创造全新的输入方案，本方案集便是[Rime输入法][]的新世纪五笔输入方案的实现；与它一见钟;情，官网地址是: https://rime.im

下面是Rime输入法在各个平台的名称：
- macOS：**鼠须管**
- Windows：**小狼亳**
- Linux：**中州韻**
- Android：**同文**
- IOS：**小鹤双拼五笔输入法**







# 5. 作者信息
**如果您在使用该方案集的过程中有遇到了问题，或者有好的建议和想法，您都可以通过以下方式联系我，期待与您的交流：**  

- **方案制作人:** 郭斌勇
- 给该仓库提交 [issues][]
- 给我 Pull requests
- **邮箱：** <guobinyong@qq.com>
- **QQ：** guobinyong@qq.com
- **微信：** keyanzhe