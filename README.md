# WifiAp8.0
注意步骤
1. 设置jar相对包路径或绝对路径
```groovy
allprojects {
    //...
    gradle.projectsEvaluated {
        tasks.withType(JavaCompile) {
            // 设置jar相对包路径或绝对路径
            options.compilerArgs.add('-Xbootclasspath/p:app/src/main/libs/WifiAp8.jar')
        }
    }
}
```

2.app/build.gradle 添加依赖
```groovy
dependencies {
    provided files('src/main/libs/WifiAp8.jar')
}
```

