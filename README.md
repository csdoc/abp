# ABP 框架

[![Build Status](http://vjenkins.dynu.net:5480/job/abp/badge/icon)](http://vjenkins.dynu.net:5480/blue/organizations/jenkins/abp/activity)

这个项目是下一代的 [ASP.NET Boilerplate](https://aspnetboilerplate.com/) Web应用程序框架. [ABP框架介绍(英文)](https://abp.io/blog/abp/Abp-vNext-Announcement) 或 [ABP框架介绍(中文)](docs/Blog-Posts/2018-09-24-Announcement/Post.cn.md).

### 开发状态

这个项目处于 **早期预览** 阶段, 并不建议在实际项目中使用它.

### 文档

查看ABP框架 <a href="docs\Index.cn.md" target="_blank">文档</a>.

### 如何编译

- 运行 `build-all.ps1`. 它将构建此存储库中的所有解决方案.

### 开发环境

#### 预先要求

- Visual Studio 2017 15.7.0+

#### 框架

框架解决方案位于`framework`文件夹下. 它没有外部依赖. 只需通过Visual Studio打开`Volo.Abp.sln`就可以开始开发.

#### 模块/模板

[模块](modules/) 和 [模板](templates/) 有自己的解决方案,并有**本地依赖**框架. 不幸的是Visual Studio在本地引用解决方案之外的项目存在一些问题. 解决方法是按照以下步骤开始开发[模块](modules/) 和 [模板](templates/):

- 在Visual Studio选项中禁用"*Automatically check for missing packages during build in Visual Studio*".

![disable-package-restore-visual-studio](docs/images/disable-package-restore-visual-studio.png)

- 当您要打开解决方案时, 请首先在解决方案的根文件夹中运行`dotnet restore`.
- 当您更改项目的依赖项时(或项目中的任何依赖项更改其依赖项), 请再次运行`dotnet restore`.

### 贡献

ABP是一个开源平台.

* 如果您发现了错误或者您有新的功能/改进想法.请打开一个[issue](https://github.com/abpframework/abp/issues/new).
* 如果要参与开发,请在开发之前创建一个问题,以便我们进行讨论.然后再创建PR.
* 对[文档](docs/Index.md)进行翻译.
