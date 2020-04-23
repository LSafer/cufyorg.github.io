<html lang="en">
    <head>
        <title>Cufy</title>
        <script>
            window.onload = function() {
              let link = top.document.createElement("link");
              link.type = "image/*";
              link.rel = "icon";
              link.href = "cufy.png";
              top.document.getElementsByTagName("head")[0].appendChild(link);
            };
        </script>
    </head>
</html> 
Cufy is a growing organization. It has few projects and all of them
about programming. Cufy is always open-source. Some of the projects
of Cufy are mentioned below:

-   ## Cufy Framework
    The main project of the cufy organization. The framework is written in java.
    The framework tries to compete with other frameworks. The cufy framework is
    focused on to be more inheritable and more reflection friendly. Making it 
    more reliable in big complex projects. The framework still not completely
    ready to be used in really big projects since it is still in the beta stage. 
    -   [Website](https://framework.cufy.org)
    -   [javadoc](https://framework.cufy.org/docs)
    -   [Github](https://github.com/cufyorg/framework)
    -   [Jitpack](https://jitpack.io/#org.cufy/framework)

-   ## Android Commons
    To extend the cufy framework more further. This repository is a part of the
    framework but designed for android. Solving some common issues in android
    application development.
    -   [Github](https://cufyorg.github.io/android-commons)
    -   [Jitpack](https://jitpack.io/#org.cufy/android-commons)

-   ## Android SettingView
    Dealing with data and settings is a bit hard when it comes to an applications
    with a lot of performance choices. The SettingView is an abstraction to
    automate the UI generating, data saving and data loading. And combining
    it with `cufy.beans` and `cufy.io.loadable` will make it more and more easier
    to deal with data in any android application locally and from the internet.
    -   [Github](https://cufyorg.github.io/android-settingview)
    -   [Jitpack](https://jitpack.io/#org.cufy/android-settingview)