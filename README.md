# Repository
aar、plugin的maven仓库

* 1.使用aar
```
	项目的build.gradle添加
	allprojects {
	    repositories {
	        ...
	        maven { url "https://raw.github.com/Frezrik/Repository/master/lilbrary" }
	    }
	}

	模块的build.gralde添加
	dependencies {
		...
	    //transitive关键字依然传递依赖
	    implementation group: 'com.frezrik.support', name: 'utils', version: '1.0', transitive: true
	}
```

* 2.使用plugin(暂无)
```
	项目的build.gradle添加
	buildscript {
		...
		repositories {
        	...
        	maven { url "https://raw.github.com/Frezrik/Repository/master/plugin" }
    	}
	    dependencies {
	        ...
	        classpath 'com.frezrik.plugin:component-build:1.0.0'
	    }
	}

	模块的build.gralde添加
	apply plugin: 'com.frezrik.plugin'
```
