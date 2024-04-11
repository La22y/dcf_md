# Mac 快速上手指南

- 按照顺序阅读、不需要配置的环境可以略过。

## 快捷键

**全局**

- 返回桌面 `command` `F3`
- **全局搜索：`Command` + `Space`** 

- 切换应用：`Command` + `Tab` 
- 退出应用：`Command` + `Q` 

**应用间**

- 切换应用 `command` + `tab`

- 隐藏应用 `command` + `h`

**应用内**

- 切换页面 `command`+ `shift` +左右

- 切换标签页：`Command` + `Shift` + `[`/`]`

- 切换窗口：`Command` + `` ` `` 

**特殊应用**

idea

- 刚刚编辑的地方 `command`+ `option`+ 左右



## 触控板与鼠标设置

- 触控板灵敏度：全局搜索 `鼠标与触控板` -> `触控板选项`
- 反转鼠标滚轮：下载开源项目 [Scroll-Reverser](https://pilotmoon.com/scrollreverser/)

## 运行环境相关配置

运行环境建议：不导入本地环境，使用应用内部环境。

- **Jetbrains**：建议下载 [ToolBox](https://www.jetbrains.com/toolbox-app/)（Jetbrains 全家桶）来进一步管理相关 IDE。
- **VScode**：官网下载 [VScode](https://code.visualstudio.com/) 进行拖拽安装。
- **Node 安装并在 VScode 中使用**：官网下载 [Node](https://nodejs.org/en) 安装引导程序完成进一步安装，VScode 插件页面搜索 Code Runner 安装，点击齿轮查看相关快捷键。

## 数据库相关环境配置

### 建议使用 docker 配置

1. Docker 官网下载 Docker DeskTop 后完成安装。

2. 各类数据系统安装运行命令，在命令行窗口执行：

   - postgres：
     - 默认用户名：postgres
     - 密码：root
     - `docker run --name postgres -e POSTGRES_PASSWORD=root -p 5432:5432 -d postgres`
   - mysql：
     - 默认用户名：root
     - 密码：root
     - `docker run --name mysql -e MYSQL_ROOT_PASSWORD=root -p 3306:3306 -d mysql:8.3.0`
   - sqlServer:
     - 默认用户名：sa
     - 密码：sqlServer@pass
     - `docker run -e "ACCEPT_EULA=Y" -e "MSSQL_SA_PASSWORD=sqlServer@pass" -p 1433:1433 --name sqlServer  -d mcr.microsoft.com/mssql/server:2022-latest`

3. 后续在 Docker DeskTop 应用 Containers 中进行统一管理运行。

4. sql

   ```
   create database your_database;
   use your_database;
   ```


## 包管理工具

mac中建议使用包管理工具 [homebrew](https://brew.sh/zh-cn/)

