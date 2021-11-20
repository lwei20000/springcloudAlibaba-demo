# springcloud-demo

```java
视频地址：https://www.bilibili.com/video/BV18E411x7eT?p=5
笔记代码：https://gitee.com/cunjinFS/SpringCloud/blob/master/pom.xml
```

# 一、springcloud基本知识

<img src="/Users/weiliang/IdeaProjects/springcloudalibaba-demo/README.assets/image-20211120162220981.png" alt="image-20211120162220981" style="zoom:25%;" />

**springboot和springcloud的匹配关系**

<img src="/Users/weiliang/IdeaProjects/springcloudalibaba-demo/README.assets/image-20211120161702538.png" alt="image-20211120161702538" style="zoom:50%;" />

<img src="/Users/weiliang/IdeaProjects/springcloudalibaba-demo/README.assets/image-20211120161956030.png" alt="image-20211120161956030" style="zoom: 25%;" />

<img src="/Users/weiliang/IdeaProjects/springcloudalibaba-demo/README.assets/image-20211120162028190.png" alt="image-20211120162028190" style="zoom:25%;" />



> tips01：pom文件跳过单元测试。点击闪电标志。

<img src="/Users/weiliang/IdeaProjects/springcloudalibaba-demo/README.assets/image-20211120164455632.png" alt="image-20211120164455632" style="zoom:33%;" />



# 二、搭建代码demo

## 2.1devtools热部署

<img src="/Users/weiliang/IdeaProjects/springcloudalibaba-demo/README.assets/image-20211120211142186.png" alt="image-20211120211142186" style="zoom:25%;" />

第一步：添加devtools的jar包到工程中

```xml
<!--devtools-->
<dependency>
  <groupId>org.springframework.boot</groupId>
  <artifactId>spring-boot-devtools</artifactId>
  <scope>runtime</scope>
  <optional>true</optional>
</dependency>
```

第二步：下列插件配置粘贴到父工程配置中

```xml
<build>
  <plugins>
    <plugin>
      <groupId>org.springframework.boot</groupId>
      <artifactId>spring-boot-maven-plugin</artifactId>
      <configuration>
        <fork>true</fork>
        <addResources>true</addResources>
      </configuration>
    </plugin>
  </plugins>
</build>
```

第二步：下列插件配置粘贴到父工程配置中

第三步：A、D、B、C全部打勾

<img src="/Users/weiliang/IdeaProjects/springcloudalibaba-demo/README.assets/image-20211120211408985.png" alt="image-20211120211408985" style="zoom:33%;" />

第四步：ctrl+shift+alt+/

<img src="/Users/weiliang/IdeaProjects/springcloudalibaba-demo/README.assets/image-20211120211550300.png" alt="image-20211120211550300" style="zoom:33%;" />\di

第五步：重启idea

## 2.2、RunDashboard配置

在workspace.xml中添加如下配置：

```xml
 <component name="RunDashboard">
    <option name="configurationTypes">
      <set>
        <option value="SpringBootApplicationConfigurationType" />
      </set>
    </option>
    <option name="ruleStates">
      <list>
        <RuleState>
          <option name="name" value="ConfigurationTypeDashboardGroupingRule" />
        </RuleState>
        <RuleState>
          <option name="name" value="StatusDashboardGroupingRule" />
        </RuleState>
      </list>
    </option>
  </component>
```

<img src="/Users/weiliang/IdeaProjects/springcloudalibaba-demo/README.assets/image-20211120223504604.png" alt="image-20211120223504604" style="zoom:33%;" />

我的mac中是service组件。

<img src="/Users/weiliang/IdeaProjects/springcloudalibaba-demo/README.assets/image-20211120224919817.png" alt="image-20211120224919817" style="zoom:33%;" />
