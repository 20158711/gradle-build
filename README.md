# gradle demo

## build.gradle文件

**apply plugin: 'java'**

    java编译插件
    
**jar**

    manifest{
        attributes 
            'Implementation-Title': 'Gradle Quickstart',
            'Implementation-Version': version,
            'Main-Class': 'Main'
    } 
    指定jar包主类
    
**uploadArchives**

    uploadArchives {
        repositories {
            flatDir {
                dirs 'repos'
            }
        }
    }
    指定jar包输出位置
    命令 gradle uploadArchives
    
**repositories**

    repositories {
        mavenCentral()
        maven {
            url "http://repo.mycompany.com/mavne2"
        }
    }
    指定仓库
    
**dependencies**

    dependencies{
        testCompile 'junit:junit:4.12'
    //    testCompile 'group': 'junit', 'name': 'junit', 'version':'4.12'
    }
    
**测试报告**

    build/reports/tests/test/index.html
   
**编码设置**

    compileJava.options.encoding='UTF-8'
    compileTestJava.options.encoding='UTF-8'
