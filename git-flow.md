## git flow 基本工作流

bug 修复分支流程 hoxfix 与 f 相同，但是是基于master开分支。

*f：feature*

|master|release|develop|f-demo|f-test|
|:---:|:---:|:---:|:---:|:---:|
|-|无|get checkout -b develop|无|无|
|-|无|-|在develop<br> get checkout -b f-demo|在develop<br> get checkout -b f-test|
|-|无|-|开发结束向 develop merge request|-|
|-|无|merge f-demo|-|开发|
|-|-|构建测试成功|删除|开发|
|-|在develop<br> git checkout -b release|-|无|开发|
|-|构建测试成功|-|无|开发|
|git merge release 并 打 [tag]|删除|git merge release |无|开发|
|-|-|-|-|git merge [tag]
