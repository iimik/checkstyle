

# checkstyle



## 插件

* [CheckStyle-IDEA](docs/plugins/CheckStyle-IDEA.md) : IDEA checkstyle 插件。

## 规则



* Imports
  * [Avoid Star Import](docs/rules/avoid-star-import.md)：禁止`import *`。
* Parameters
  * [Final Parameters](docs/rules/final-parameters)：参数使用`final`修饰。



## Names

```xml

<module name="TreeWalker">

    <!-- Names -->
    <module name="PackageName">
        <property name="format" value="^[a-z]+(\.[a-z][a-z0-9]*)*$"/>
        <message key="name.invalidPattern" value="Package name ''{0}'' must match pattern ''{1}''."/>
    </module>
    <module name="TypeName">
        <property name="tokens" value="CLASS_DEF, INTERFACE_DEF, ENUM_DEF, ANNOTATION_DEF"/>
        <message key="name.invalidPattern" value="Type name ''{0}'' must match pattern ''{1}''."/>
    </module>
    <module name="MemberName">
        <property name="format" value="^[a-z][a-z0-9][a-zA-Z0-9]*$"/>
        <message key="name.invalidPattern" value="Member name ''{0}'' must match pattern ''{1}''."/>
    </module>
    <module name="ParameterName">
        <property name="format" value="^[a-z]([a-z0-9][a-zA-Z0-9]*)?$"/>
        <message key="name.invalidPattern" value="Parameter name ''{0}'' must match pattern ''{1}''."/>
    </module>
    <module name="LambdaParameterName">
        <property name="format" value="^[a-z]([a-z0-9][a-zA-Z0-9]*)?$"/>
        <message key="name.invalidPattern" value="Lambda parameter name ''{0}'' must match pattern ''{1}''."/>
    </module>
    <module name="CatchParameterName">
        <property name="format" value="^[a-z]([a-z0-9][a-zA-Z0-9]*)?$"/>
        <message key="name.invalidPattern" value="Catch parameter name ''{0}'' must match pattern ''{1}''."/>
    </module>
    <module name="LocalVariableName">
        <property name="format" value="^[a-z]([a-z0-9][a-zA-Z0-9]*)?$"/>
        <message key="name.invalidPattern" value="Local variable name ''{0}'' must match pattern ''{1}''."/>
    </module>
    <module name="ClassTypeParameterName">
        <property name="format" value="(^[A-Z][0-9]?)$|([A-Z][a-zA-Z0-9]*[T]$)"/>
        <message key="name.invalidPattern" value="Class type name ''{0}'' must match pattern ''{1}''."/>
    </module>
    <module name="MethodTypeParameterName">
        <property name="format" value="(^[A-Z][0-9]?)$|([A-Z][a-zA-Z0-9]*[T]$)"/>
        <message key="name.invalidPattern" value="Method type name ''{0}'' must match pattern ''{1}''."/>
    </module>
    <module name="InterfaceTypeParameterName">
        <property name="format" value="(^[A-Z][0-9]?)$|([A-Z][a-zA-Z0-9]*[T]$)"/>
        <message key="name.invalidPattern" value="Interface type name ''{0}'' must match pattern ''{1}''."/>
    </module>
</module>
```



