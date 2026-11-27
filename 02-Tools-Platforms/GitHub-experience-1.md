# GitHub体验笔记

## 1. 背景与目标

- **时间**：2026-11-22  
- **目标**：了解 GitHub 的主要功能，熟悉 GitHub 仓库的基本操作与维护规范，掌握``.gitignore`` 的使用，完成本地与远程仓库的同步  
- 环境： Windows/Git Bash  

## 2. 核心操作流程  

主要完成的任务如下：

1. **GitHub 基础了解**：

- **GitHub 是**一个基于 Git 的代码托管与写作平台。Git 是本地工具，GitHub 是云端服务。  
- GitHub 主要用途有版本控制与备份、多人协作、参与开源、项目管理等。  
- **Fork** 把别人仓库复制一份到自己 GitHub 账号下  
-  **Pull Request(PR)** 修改拉取合并请求。常见于协作流程，在 Fork,Clone,Branch,修改并Commit,Push 之后，把改动合并到原作者的仓库里。  
- **了解来源**：B站视频， DeepSeek AI，学习网站：  https://learngitbranching.js.org/?locale=zh_CN

2. **GitHub 基本操作**  

- Fork(复刻)  
- Clone(克隆)  
- Fetch(下载) 仅仅进行下载操作，不改变本地原仓库状态
    - git fetch前：
    
    ![屏幕截图 2026-11-23 203313.png](https://note-pics-1538697009.cos.ap-guangzhou.myqcloud.com/img/20261123204624287.png)
    
	- git fetch后：
	
	![屏幕截图 2026-11-23 203256.png](https://note-pics-1538697009.cos.ap-guangzhou.myqcloud.com/img/20261123204807947.png)
	
- Pull(拉取)  git pull近乎是git fetch与下一次合并的简写
- Branch(建分支)  
	```
	git branch xxx
	git switch xxx
	git commit
	```
	新建分支并切换分支到新分支上，再往新分支里提交新的东西
	
- Commit(提交)  
    ```
    git add .
    git commit -m "commit message"
    git push
    ```
    
    - gitignore：告诉Git **``.gitignore``** 的东西不要上传到 GitHub，被 commit 过的文件必须先用 ``git rm --cached`` 从版本库中踢出去，``.gitignore`` 才能生效  
    - **commit message**：规范``<type>(<scope>):<subject>`` + 空行 + ``<body>`` + 空行 + ``<footer>``  
        -  Type(类型)  
        - Scope(作用域)  
        - Subject(主题)  
        - Body(正文)  
        - Footer(脚注)  
        - 硬性限制：任何一行不得超过100字符  
-  Push(推送)  
    ``git push`` 
-  发起PR(请求把Branch的改动合并到原作者的仓库里)  
    - 常见PR状态  
        - Open：正在讨论和审查中。  
        - Draft：草稿状态  
        - Merged：合并成功。  
        - Closed：被关闭了。
  - Merge(合并)
	  
	- 两个分支都有新的commit
	
	![屏幕截图 2026-11-27 215204.png](https://note-pics-1538697009.cos.ap-guangzhou.myqcloud.com/img/20261127215903245.png)
	
	- 把 bugFix 合并到 main 里
	``git merge buFix``
	
	![屏幕截图 2026-11-27 215229.png](https://note-pics-1538697009.cos.ap-guangzhou.myqcloud.com/img/20261127220345154.png)
	
	- 把 main 分支合并到 bugFix
	```
	git switch bugFix
	git merge main
	```
	
	![屏幕截图 2026-11-27 215245.png](https://note-pics-1538697009.cos.ap-guangzhou.myqcloud.com/img/20261127220646160.png)
	

## 3. Markdown 书写  

- 所运用的规范  
    - 标题严格按层级书写，不跳级  
    - 代码的格式  
    - 中英文间空格  
    - 图片前后空行