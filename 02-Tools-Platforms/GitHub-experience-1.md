# GitHub体验笔记

## 1. 背景与目标

- **时间**：2026-11-22  
- **目标**：了解 GitHub 的主要功能，熟悉 GitHub 仓库的基本操作与维护规范，掌握``.gitignore`` 的使用，完成本地与远程仓库的同步  
- 环境： Windows/Git Bash  

## 2. 核心操作流程  

主要完成的任务如下：

1. **GitHub 基础了解：  **

- **GitHub 是**一个基于 Git 的代码托管与写作平台。Git 是本地工具，GitHub 是云端服务。  
- GitHub 主要用途有版本控制与备份、多人协作、参与开源、项目管理等。  
- **Fork** 把别人仓库复制一份到自己 GitHub 账号下  
-  **Pull Request(PR)** 修改拉取合并请求。常见于协作流程，在 Fork,Clone,Branch,修改并Commit,Push 之后，把改动合并到原作者的仓库里。  
- **了解来源**有B站视频和 DeepSeek AI。  

2. **GitHub 基本操作**  

- Fork(复刻)  
- Clone(克隆)  
- Pull(拉取)  
- Branch(建分支)  
- Commit(提交)  
 - gitignore：告诉Git **``.gitignore``** 的东西不要上传到 GitHub，被 commit 过的文件必须先用 ``git rm --cached`` 从版本库中踢出去，``.gitignore`` 才能生效  
- **commit message**：规范``<type>(<scope>):<subject>`` + 空行 + ``<body>`` + 空行 + ``<footer>``  
   -  Type(类型)  
   - Scope(作用域)  
   - Subject(主题)  
   - Body(正文)  
   - Footer(脚注)  
   - 硬性限制：任何一行不得超过100字符  
-  Push(推送)  
-  发起PR(请求把Branch的改动合并到原作者的仓库里)  
 - 常见PR状态  
    Open：正在讨论和审查中。  
    Draft：草稿状态  
    Merged：合并成功。  
    Closed：被关闭了。
  
## 3. Markdown 书写  

- 所运用的规范  
 - 标题严格按层级书写，不跳级  
 - 代码的格式  
 - 中英文间空格  
 - 换行要至少在前一行末尾加