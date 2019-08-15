### 基础设置
#### jdk
`File -> other settings -> Default Project Structure -> SDKs`

#### Project SDK
`File -> other settings -> Default  Project Structure -> Project`

#### maven 
`File -> other settings -> Default settings -> maven`  

勾选：`Always update snapshots`  (慎重)

自定义maven命令： Maven Projects -> Lifecycle -> 右击 create

#### tomcat
Run Configurations -> + -> tomcat
热部署： 添加 .war exploded

#### springboot热部署
IDEA: `ctrl + shift + alt + /` -> Registry -> 勾选 Compiler.automake.allow.when.app.running    
#### 其他设置
自动编译：`Default Settings -> Build -> Build project automatically`

字符集：`Default Settings -> Editor -> File Encodings`

import * 问题：`Other Settings -> Default Settings  -> Code Style -> Java -> Imports -> Class count to use import with *` 设置为 999

mapper注入警告问题：`Settings -> Editor -> Inspections -> Spring -> Spring Core -> Code-> Autowiring for Bean Class` [Warning]

自动优化导入的包:   
   - 勾选:`Settings -> Editor -> General -> Auto Import  Optimize imports on the fly` 自动清楚没有用到的包  
   - 勾选:`Settings -> Editor -> General -> Auto Import  Add unambiguous imports on the fly`  自动优化导入的包

显示空格：`Settings -> Editor -> General -> Appearance -> Show whitespaces`

取消参数提示：`Settings -> Editor -> General -> Appearance -> Show parameter name hints`

Tab设置为空格：`Settings -> Editor -> Code Style -> Java -> Tabs and Indents ` 

- 勾选 Smart tabs,
- 取消勾选Use tab character

注释中描述后面去掉空行：`Settings -> Code Style -> Java -> JavaDoc -> Blank lines` 取消勾选After desc 

提示序列化id：`Settings -> inspections -> serializable class without` 勾选

Lombok注解支持：`Build -> Compiler -> Annotation Processors Enable....`

Terminal修改为git终端后不支持中文：[支持中文](https://www.cnblogs.com/feihualuoshi/p/7908356.html)

#### File and Code Templates

```
/**
 * TODO
 * @author Menng
 * @date ${DATE} ${TIME}
 */
```

#### Live Templates

```
*
 * created by Menng on $DATE$ $TIME$
 */
```



### 快捷键

#### 常用

- alt + enter 提示
- ctrl + 左键  接口
- ctrl + h 显示类的子层级
- ctrl + n 查找类
- ctrl + q 显示方法说明
- ctrl + alt + 左键 实现类
- ctrl + alt + o 清除无用的import
- ctrl + alt + l 格式化代码
- ctrl + alt + b 调转到实现
- ctrl + alt + t suround with
- ctrl + shift + z 向前
- ctrl + shift + n 查找文件
- ctrl + shift + F12 窗口最大化
- ctrl + shift + u 大小写切换
- shift + esc 收起当前views
- ctrl + F12 类方法列表
- ctrl + F2 关闭应用
- 右键Diagrams-> Show Diagram 查看继承关系 按着Alt放大镜
- 更多[http://wiki.jikexueyuan.com/project/intellij-idea-tutorial/keymap-introduce.html](http://wiki.jikexueyuan.com/project/intellij-idea-tutorial/keymap-introduce.html)
- 调试
    ```
    F9            resume programe 恢复程序  
    Alt+F10       show execution point 显示执行断点  
    F8            Step Over 相当于eclipse的f6      跳到下一步  
    F7            Step Into 相当于eclipse的f5就是  进入到代码  
    Alt+shift+F7  Force Step Into 这个是强制进入代码  
    Shift+F8      Step Out    相当于eclipse的f8跳到下一个断点，也相当于eclipse的f7跳出函数  
    Atl+F9        Run To Cursor 运行到光标处   
    ctrl+shift+F9   debug运行java类  
    ctrl+shift+F10  正常运行java类
    ```
- https://www.cnblogs.com/snifferhu/p/7274548.html

#### 自定义快捷键

- Alt + D 全屏切换
- ctrl + shift + o 刷新依赖



### 插件
- lombok 
- Maven Helper 用来分析依赖树  
- Free Mybatis plugin 方便从类跳转到xml
- AceJump 页面内跳转  
- Key promoter X 快捷键提示
- Statistic 统计代码
- Iedis redis可视化工具，收费[Guide](https://www.codesmagic.com/iedis/userguide/getting-started)
- JProfiler 分析工具



### 新版Run Dashboard打开方法

打开`.idea/workspace.xml`文件，接下来找到`<component name="RunDashboard">`，加入如下：
```
<option name="configurationTypes">  
      <set>  
        <option value="SpringBootApplicationConfigurationType" />  
      </set>  
 </option>  
```
[参考](https://www.cnblogs.com/yangtianle/p/8818255.html)



### 控制台乱码问题

如果网上的结果无法解决你的问题，找到你的idea配置文件(非安装目录的配置文件)， `.IntelliJIdea2019.2\config\idea64.exe.vmoptions` 在这里修改你的编码配置。 