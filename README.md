# OpenConext-oidc-themevanilla

Vanilla RCIAM theme for [OpenConext](https://github.com/rciam/OpenConext-oidc), which is implementation of a OpenID Connect server based on the MITREid Connect server

## Install

To install the theme you must copy the changes were made in webapp directory
 
```
git clone https://github.com/rciam/OpenConext-oidc-themevanilla.git
cp -a <path to OpenConect-oidc-themevanilla>/oidc-server <path to OpenConect-oidc>/oidc-server
```

Edit server-config.xml which is located in:

`<path to OpenConect-oidc>/oidc-server/src/main/webapp/WEB-INF/server-config.xml`

and add the property to override the old messages without losing them

```
<!-- This property sets the set of namespaces for language translation files. The default is "messages". These are checked in the order presented here. -->
<property name="languageNamespaces">
    <list>
        <value>theme</value>
        <value>custom</value>
        <value>messages</value>
    </list>
</property>
```

To modify or override the texts in .tag files edit the following file

`<path to OpenConect-oidc>/oidc-server/src/main/webapp/resources/js/locale/en/theme.json`

Note: If you have modified the files in your webapp directory, make sure to backup your changes and apply them to the corresponding files.