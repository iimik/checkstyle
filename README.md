# CheckStyle



## OverView

![CheckStyle](http://assets.processon.com/chart_image/5fd4b810e401fd06ddbe92a9.png)

[CheckStyle Mind](https://www.processon.com/view/link/5fd770515653bb06f33e1133)



## File

### FileTabCharacter

文件中禁止出现`\t`字符。

```xml
<!--文件Tab字符 -->
<module name="FileTabCharacter">
    <property name="eachLine" value="true"/>
</module>
```

### FileLength

```xml
<!--文件长度-->
<module name="FileLength">
    <property name="max" value="1500"/>
</module>
```

### LineLength

```xml
<!-- 单行长度-->
<module name="LineLength">
    <property name="fileExtensions" value="java"/>
    <property name="max" value="120"/>
    <property name="ignorePattern" value="^package.*|^import.*|a href|href|http://|https://|ftp://"/>
</module>
```

### NewlineAtEndOfFile

```xml
<!-- 以空行结尾 -->
<module name="NewlineAtEndOfFile"/>
```

* 示例

```java
public class JavaFile {
    
}

```

### NoCodeInFile

```xml
<!-- 空文件 -->
<module name="NoCodeInFile"/>
```

### OuterTypeFileName

```xml
<!-- 类文件名称 -->
<module name="OuterTypeFilename"/>
```

* 示例: `MyjavaClass.java`

```java
public class MyJavaClass {}
```

### AvoidEscapedUnicodeCharacters

```xml
<!-- 避免转义的Unicode字符 -->
<module name="AvoidEscapedUnicodeCharacters">
    <property name="allowEscapesForControlCharacters" value="true"/>
    <property name="allowByTailComment" value="true"/>
    <property name="allowNonPrintableEscapes" value="true"/>
</module>
```



## Name

### PackageName

```xml
<module name="PackageName">
    <message key="name.invalidPattern"
        value="Package name ''{0}'' must match pattern ''{1}''."/>
    <property name="format" value="^[a-z]+(\.[a-z][a-z0-9]*)*$"/>
</module>
```

### TypeName

```xml
<module name="TypeName">
    <message key="name.invalidPattern"
        value="Type name ''{0}'' must match pattern ''{1}''."/>
    <property name="tokens" value="CLASS_DEF, INTERFACE_DEF, ENUM_DEF,
            ANNOTATION_DEF, RECORD_DEF"/>
</module>
```

### MethodName

```xml
<!-- 方法名称 -->
<module name="MethodName">
    <message key="name.invalidPattern"
        value="Method name ''{0}'' must match pattern ''{1}''."/>
    <property name="format" value="^[a-z][a-z0-9][a-zA-Z0-9_]*$"/>
</module>
```

### ParameterName

```xml
<!--  参数名称 -->
<module name="ParameterName">
    <message key="name.invalidPattern"
        value="Parameter name ''{0}'' must match pattern ''{1}''."/>
    <property name="format" value="^[a-z]([a-z0-9][a-zA-Z0-9]*)?$"/>
</module>
```

### MemberName

```xml
<!--  成员名称 -->
<module name="MemberName">
    <message key="name.invalidPattern"
        value="Member name ''{0}'' must match pattern ''{1}''."/>
    <property name="format" value="^[a-z][a-z0-9][a-zA-Z0-9]*$"/>
</module>
```

### LambdaParameterName

```xml
<!--  Lambda 参数名称 -->
<module name="LambdaParameterName">
    <message key="name.invalidPattern"
        value="Lambda parameter name ''{0}'' must match pattern ''{1}''."/>
    <property name="format" value="^[a-z]([a-z0-9][a-zA-Z0-9]*)?$"/>
</module>
```

### CatchParameterName

```xml
<!--  Catch 参数名称 -->
<module name="CatchParameterName">
    <message key="name.invalidPattern"
        value="Catch parameter name ''{0}'' must match pattern ''{1}''."/>
    <property name="format" value="^[a-z]([a-z0-9][a-zA-Z0-9]*)?$"/>
</module>
```



### LocalVariableName

```xml
<!--  本地变量名称 -->
<module name="LocalVariableName">
    <message key="name.invalidPattern"
        value="Local variable name ''{0}'' must match pattern ''{1}''."/>
    <property name="format" value="^[a-z]([a-z0-9][a-zA-Z0-9]*)?$"/>
</module>
```

### PatternVariableName

```xml
<module name="PatternVariableName">
    <message key="name.invalidPattern"
        value="Pattern variable name ''{0}'' must match pattern ''{1}''."/>
    <property name="format" value="^[a-z]([a-z0-9][a-zA-Z0-9]*)?$"/>
</module>
```

### ClassTypeParameterName

```xml
<module name="ClassTypeParameterName">
    <message key="name.invalidPattern"
        value="Class type name ''{0}'' must match pattern ''{1}''."/>
    <property name="format" value="(^[A-Z][0-9]?)$|([A-Z][a-zA-Z0-9]*[T]$)"/>
</module>
```

### RecordTypeParameterName

```xml
<module name="RecordTypeParameterName">
    <message key="name.invalidPattern"
        value="Record type name ''{0}'' must match pattern ''{1}''."/>
    <property name="format" value="(^[A-Z][0-9]?)$|([A-Z][a-zA-Z0-9]*[T]$)"/>
</module>
```

### MethodTypeParameterName

```xml
<module name="MethodTypeParameterName">
    <message key="name.invalidPattern"
        value="Method type name ''{0}'' must match pattern ''{1}''."/>
    <property name="format" value="(^[A-Z][0-9]?)$|([A-Z][a-zA-Z0-9]*[T]$)"/>
</module>
```

### InterfaceTypeParameterName

```xml
<module name="InterfaceTypeParameterName">
    <message key="name.invalidPattern"
        value="Interface type name ''{0}'' must match pattern ''{1}''."/>
    <property name="format" value="(^[A-Z][0-9]?)$|([A-Z][a-zA-Z0-9]*[T]$)"/>
</module>
```

## Package

### JavadocPackage

```xml
<!-- 缺少 package-info.java 文件 -->
<module name="JavadocPackage"/>
```

### PackageDeclaration

```xml
<!-- 包声明 -->
<module name="PackageDeclaration"/>
```

## Import

### AvoidStarImport

```xml
<!--避免*号导入-->
<module name="AvoidStarImport"/>
```

* 示例

```java
import java.util.*;
```

### Avoid Static Import

```xml
<!-- 避免静态导入 -->
<module name="AvoidStaticImport">
    <property name="excludes" value="org.junit.jupiter.api.Assertions.*,org.junit.*"/>
</module>
```

### IllegalImport

```xml
<!-- 非法导入 -->
<module name="IllegalImport"/>
```

* 示例

```java
import sun.*;
```

### RedundantImport

```xml
<!-- 多余导入 -->
<module name="RedundantImport"/>
```

* 示例

```java
import java.lang.Object;
```

### UnusedImprts

```xml
<!-- 未使用导入 -->
<module name="UnusedImports"/>
```

## Modifiers

### ModifierOrder

```xml
<!-- ModifierOrder -->
<module name="ModifierOrder"/>
```

### RedundantModifier

```xml
<!-- 多余的修饰符 -->
<module name="RedundantModifier"/>
```

* 示例

```java
class MyClass {
    publuc MyClass(){
        // 构造函数没有必要声明为 final
    }
}
```



## Class

### DesignForExtension

```xml
<!-- 为扩展设计 -->
<module name="DesignForExtension"/>
```

### FinalClass

```xml
<!-- 私有构造函数的类必需声明为 final -->
<module name="FinalClass"/>
```

### HideUtilityClassConstructor

```xml
<!-- 工具类的构造函数应该被声明为 private -->
<module name="HideUtilityClassConstructor"/>
```

### InnerTypeLast

```xml
<!-- 内部类型声明在最后 -->
<module name="InnerTypeLast"/>
```

### InterfaceIsType

```xml
<!-- 接口必须有方法 -->
<module name="InterfaceIsType">
    <property name="allowMarkerInterfaces" value="true"/>
</module>
```

### MutableException

```xml
<!-- MutableException -->
<module name="MutableException"/>
```

### One Top Level Class

```xml
<!-- 只有一个顶级类 -->
<module name="OneTopLevelClass"/>
```

### AnonInnerLength

```xml
<!-- 内部类名称长度 -->
<module name="AnonInnerLength">
    <property name="max" value="60"/>
</module>
```

### NoClone

```xml
<!-- Blocks -->
<module name="NoClone"/>
```

### NoFinalizer

```xml
<!-- Blocks -->
<module name="NoFinalizer"/>
```

### Super Clone

```xml
<!-- Blocks -->
<module name="SuperClone"/>
```

### Super Finalize

```xml
<!-- Blocks -->
<module name="SuperFinalize"/>
```

### EqualsHashCode

```xml
<!-- 是否同时重写了 equals hashCode -->
<module name="EqualsHashCode"/>
```



## Enum

### NoEnumTrailingComma

```xml
<!-- 枚举结尾逗号 -->
<module name="NoEnumTrailingComma"/>
```

```java
publci enum MyEnum {
    ITEM,
}
```



### UnnecessarySemicolonInEnumeration

```xml
<!-- 枚举中不必要的分号 -->
<module name="UnnecessarySemicolonInEnumeration"/>
```

```java
public enum MyEnum {
    ITEM;
}
```



## Array

### ArrayTypeStyle

```xml
<!-- 数组风格 -->
<module name="ArrayTypeStyle"/>
```

* 示例

```java
int[] nums; // OK
int nums[]; // ERROR
```

### ArrayTrailingComma

```xml
<!-- 数组尾部逗号 -->
<module name="ArrayTrailingComma"/>
```

### NoArrayTrailingComma

```xml
<!-- 数组尾部逗号 -->
<module name="NoArrayTrailingComma"/>
```



## Member

### DeclarationOrder

```xml
<!-- 定义顺序 -->
<module name="DeclarationOrder"/>
```

### ExplicitInitialization

```xml
<!-- 显式初始化 -->
<module name="ExplicitInitialization">
    <property name="onlyObjectReferences" value="true"/>
</module>
```



## Method

### MethodCount

```xml
<!-- 方法数量 -->
<module name="MethodCount">
    <property name="maxTotal" value="200"/>
    <property name="maxPrivate" value="100"/>
    <property name="maxPackage" value="100"/>
    <property name="maxProtected" value="100"/>
    <property name="maxPublic" value="200"/>
</module>
```

### MethodLength

```xml
<!-- 方法长度 -->
<module name="MethodLength">
    <property name="max" value="100"/>
    <property name="countEmpty" value="true"/>
</module>
```

### ExecutableStatementCount

```xml
<!-- 可执行语句数量 -->
<module name="ExecutableStatementCount">
    <property name="max" value="100"/>
    <property name="tokens" value="CTOR_DEF,METHOD_DEF"/>
</module>
```

### Return Count

```xml
<!-- Return 次数 -->
<module name="ReturnCount">
    <property name="max" value="10"/>
    <property name="maxForVoid" value="10"/>
</module>
```



## Parameter

### ParameterNumber

```xml
<!-- 参数数量 -->
<module name="ParameterNumber">
    <property name="max" value="7"/>
    <property name="ignoreOverriddenMethods" value="true"/>
</module>
```

### FinalParameters

```xml
<!-- 参数 final 修饰 -->
<module name="FinalParameters"/>
```

## Variable

### MultipleVariableDeclarations

```xml
<!-- 多个变量声明 -->
<module name="MultipleVariableDeclarations"/>
```

### VariableDeclarationUsageDistance

```xml
<!-- 变量声明与使用 -->
<module name="VariableDeclarationUsageDistance"/>
```

### FinalLocalVariable

```xml
<!-- 局部变量声明为 final -->
<module name="FinalLocalVariable"/>
```

### OneStatementPerLine

```xml
<!-- 每行一个声明 -->
<module name="OneStatementPerLine"/>
```

### ModifiedControlVariable

```xml
<!-- 修改控制变量 -->
<module name="ModifiedControlVariable"/>
```

### MultipleStringLiterals

```xml
<!-- String 字面量出现次数 -->
<module name="MultipleStringLiterals">
    <property name="allowedDuplicates" value="50"/>
</module>
```

### UpperEll

```xml
<!-- Long 使用大写L -->
<module name="UpperEll"/>
```

* 示例

```java
long num = 123L;
```





## Regexp



### 禁止 System.out.print

```xml
<!-- 禁止 System.out.print-->
<module name="RegexpMultiline">
    <property name="id" value="sout"/>
    <property name="format" value="System\.(out)|(err)\.print"/>
    <property name="message" value="System.out.print 方法不允许使用"/>
</module>
```

### 禁止 e.printStackTrace

* 配置

```xml
<!-- 禁止 e.printStackTrace -->
<module name="RegexpMultiline">
    <property name="id" value="printStackTrace"/>
    <property name="format" value="\.printStackTrace\("/>
    <property name="message" value="e.printStackTrace(**) 方法不允许使用"/>
</module>
```

* 示例

```java
try{
    
}catch(Exception e){
    // 应使用 logger.error/warn 替换 e.printStackTrace
    e.printStackTrace();
}
```

## 代码

### Avoid Double Brace Initialization

```xml
<!-- 避免双括号初始化 -->
<module name="AvoidDoubleBraceInitialization"/>
```

### Avoid Inline Conditionals 

```xml
<!--  避免三元表达式 -->
<module name="AvoidInlineConditionals"/>
```

### Avoid No Arguments Super Constructor Call

```xml
<!-- 避免无参数的父类构造函数调用 -->
<module name="AvoidNoArgumentSuperConstructorCall"/>
```

### Covariant Equals

```xml
<!-- Blocks -->
<module name="CovariantEquals"/>
```

### Declaration Order

```xml
<!-- 定义顺序 -->
<module name="DeclarationOrder"/>
```

### Default Comes Last

```xml
<!-- Default 声明在最后 -->
<module name="DefaultComesLast"/>
```

### Equal Avoid Null

```xml
<!-- 等于避免为空 -->
<module name="EqualsAvoidNull"/>
```

* 示例

```java
String name = null;
if(name.equals("Spring")){
    // maybe throw NPE
}
```

### ExplicitInitialization

```xml
<!-- 显式初始化 -->
<module name="ExplicitInitialization">
    <property name="onlyObjectReferences" value="true"/>
</module>
```

### FallThrough

```xml
<!-- Switch case 贯穿 -->
<module name="FallThrough"/>
```

### Missing Switch Default

```xml
<!-- 缺少 Switch Default -->
<module name="MissingSwitchDefault"/>
```

### Hidden Field

```xml
<!-- 隐藏属性 -->
<module name="HiddenField">
    <property name="tokens"
        value="VARIABLE_DEF , PATTERN_VARIABLE_DEF , LAMBDA , RECORD_COMPONENT_DEF "/>
    <property name="ignoreConstructorParameter" value="true"/>
    <property name="ignoreSetter" value="true"/>
    <property name="setterCanReturnItsClass" value="true"/>
</module>
```

### Illegal Catch

```xml
<!-- 非法捕获 -->
<module name="IllegalCatch"/>
```

### Illegal Instantiation

```xml
<!-- 非法初始化 -->
<module name="IllegalInstantiation">
    <property name="classes" value="java.lang.Boolean"/>
</module>
```

### Illegal Throws

```xml
<!-- 非法抛出 -->
<module name="IllegalThrows"/>
```

### IllegalToken

```xml
<!-- Blocks -->
<module name="IllegalToken"/>
```

### IllegalTokenText

```xml
<!-- Blocks -->
<module name="IllegalTokenText"/>
```

### Illeagal Type

```xml
<!-- Blocks -->
<module name="IllegalType"/>
```

### InnerAssignment

```xml
<!-- Blocks -->
<module name="InnerAssignment"/>
```

### Magic Number

```xml
<!-- 魔术数字 -->
<module name="MagicNumber">
    <property name="constantWaiverParentToken" value="EXPR"/>
    <property name="ignoreNumbers" value="-1,0,1,2"/>
    <property name="ignoreHashCodeMethod" value="true"/>
    <property name="ignoreAnnotation" value="true"/>
    <property name="ignoreFieldDeclaration" value="true"/>
    <property name="ignoreAnnotationElementDefaults" value="true"/>
</module>
```

### PackageDeclaration

```xml
<!-- Blocks -->
<module name="PackageDeclaration"/>
```

### ParameterAssignment

```xml
<!-- Blocks -->
<module name="ParameterAssignment"/>
```

### Require This

```xml
<!-- Blocks -->
<module name="RequireThis"/>
```

### SimplifyBoolean Expression

```xml
<!-- 简化布尔表达式 -->
<module name="SimplifyBooleanExpression"/>
```

### StringLiteralEquality

```xml
<!-- 字符串文字平等 -->
<module name="StringLiteralEquality"/>
```

### UnnecessarySemicolonAfterOuterTypeDeclaration

```xml
<!-- Blocks -->
<module name="UnnecessarySemicolonAfterOuterTypeDeclaration"/>
```

### UnnecessarySemicolonAfterTypeMemberDeclaration

```xml
<!-- Blocks -->
<module name="UnnecessarySemicolonAfterTypeMemberDeclaration"/>
```

### UnnecessarySemicolonInEnumeration

```xml
<!-- 枚举中不必要的分号 -->
<module name="UnnecessarySemicolonInEnumeration"/>
```

### UnnecessarySemicolonInTryWithResources

```xml
<!-- Blocks -->
<module name="UnnecessarySemicolonInTryWithResources"/>
```

### VariableDeclarationUsageDistance

```xml
<!-- Blocks -->
<module name="VariableDeclarationUsageDistance"/>
```

## Block 代码块

### LambdaBodyLength

```xml
<!-- Lambda 体长度 -->
<module name="LambdaBodyLength">
    <property name="max" value="100"/>
</module>
```

### NestedForDepth

```xml
<!-- for 嵌套次数 -->
<module name="NestedForDepth">
    <property name="max" value="3"/>
</module>
```

### NestedIfDepth

```xml
<!-- if 嵌套次数 -->
<module name="NestedIfDepth">
    <property name="max" value="3"/>
</module>
```

### NestedTryDepth

```xml
<!-- try 嵌套次数 -->
<module name="NestedTryDepth">
    <property name="max" value="3"/>
</module>
```

### AvoidNestedBlocks

```xml
<!-- 避免内部块 -->
<module name="AvoidNestedBlocks">
    <property name="allowInSwitchCase" value="false"/>
</module>
```

### Empty Statement

```xml
<!-- 空行 -->
<module name="EmptyStatement"/>
```

### EmptyBlock

```xml
<!-- 空块 -->
<module name="EmptyBlock">
    <property name="option" value="TEXT"/>
    <property name="tokens"
        value="LITERAL_TRY, LITERAL_FINALLY, LITERAL_IF, LITERAL_ELSE, LITERAL_SWITCH"/>
</module>
```

### EmptyCatchBlock

```xml
<!-- 空Catch块 -->
<module name="EmptyCatchBlock">
    <property name="exceptionVariableName" value="expected"/>
</module>
```

## Other

### AvoidDoubleBraceInitialization

```xml
<!-- 避免双括号初始化 -->
<module name="AvoidDoubleBraceInitialization"/>
```

* 示例

```java

```

### AvoidInlineConditionals

```xml
<!--  避免三元表达式 -->
<!--        <module name="AvoidInlineConditionals"/>-->
```

* 示例

```java
int a = bool ? 1 : 0;
```

### IllegalInstantiation

```
<!-- 非法实例化 -->
<module name="IllegalInstantiation">
    <property name="classes" value="java.lang.Boolean"/>
</module>
```

* 示例

```java
boolean = new Boolean(false);
```

### SimplifyBooleanExpression

```xml
<!-- 简化布尔表达式 -->
<module name="SimplifyBooleanExpression"/>
```

* 示例

```java
if(bool == true){
    // do something
}
// ==> 
if(bool){
    // do something
}
```

### UnnecessaryParentheses

```xml
<!-- 不必要的括号 -->
<module name="UnnecessaryParentheses"/>
```

* 示例

```java
int a = (1 + 1);
```

### BooleanExpressionComplexity

```xml
<!-- 布尔表达式数量 -->
<module name="BooleanExpressionComplexity">
    <property name="max" value="5"/>
</module>
```



## 注释

### CommentsIndentation

```xml
<!-- 注释对齐 -->
<module name="CommentsIndentation">
    <property name="tokens" value="SINGLE_LINE_COMMENT, BLOCK_COMMENT_BEGIN"/>
</module>
```

### TrailingComment

```xml
<!-- 行尾注释 -->
<module name="TrailingComment"/>
```

### TodoComment

```xml
<!-- TODO -->
<module name="TodoComment">
    <property name="format" value="(TODO)|(FIXME)"/>
</module>
```



## 插件

* [CheckStyle-IDEA](docs/plugins/CheckStyle-IDEA.md) : IDEA checkstyle 插件。

### Maven CheckStyle Plugin

[![Maven Central](https://img.shields.io/maven-central/v/org.apache.maven.plugins/maven-checkstyle-plugin?label=maven-plugin)](https://mvnrepository.com/artifact/org.apache.maven.plugins/maven-checkstyle-plugin)
[![Maven Central](https://img.shields.io/maven-central/v/com.puppycrawl.tools/checkstyle?label=checkstyle)](https://mvnrepository.com/artifact/com.puppycrawl.tools/checkstyle)



```xml
<plugin>
    <artifactId>maven-checkstyle-plugin</artifactId>
    <configuration>
        <!-- Check style file path -->
        <configLocation>checkstyle.xml</configLocation>
        <!-- include test source -->
        <consoleOutput>true</consoleOutput>
        <includeTestSourceDirectory>true</includeTestSourceDirectory>
    </configuration>
    <dependencies>
        <!-- https://mvnrepository.com/artifact/com.puppycrawl.tools/checkstyle -->
        <dependency>
            <artifactId>checkstyle</artifactId>
            <groupId>com.puppycrawl.tools</groupId>
            <version>8.38</version>
        </dependency>
    </dependencies>
    <executions>
        <execution>
            <goals>
                <goal>check</goal>
            </goals>
            <id>validate</id>
            <phase>validate</phase>
        </execution>
    </executions>
    <groupId>org.apache.maven.plugins</groupId>
    <version>${maven-checkstyle-plugin.version}</version>
</plugin>
```



## Git Hook



### pre-commit

```shell
#!/bin/sh
#execute shell before commit,check the code


# mvn checkstyle:check
mvn checkstyle:check
#得到checkstyle检测结果，没有代码规范问题 执行结果为0；有代码规范问题 执行结果为非0
checkstyle_result=$?
if [ $checkstyle_result -eq 0 ]
then 
    echo "项目执行checkstyle检测成功!!!"
else    
    echo "提交失败，源于项目存在代码规范问题（mvn checkstyle:check）"
    echo "请查看target目录下的checkstyle-result.html文件得知详情"
    exit 1
fi
```



