# ConfigPrivatePod
本脚本修改自[casatwy/ConfigPrivatePod](https://github.com/casatwy/ConfigPrivatePod)

⚠️：需使用fastlne进行pod发版


1. git clone git@github.com:Yunlou1995/ConfigPrivatePod.git
2. 新建业务工程和category工程
4. git新建Repo，页面先不要关闭，下一条命令需要用到（如果没有私有源，记得新建一个Repo作为私有源）
5. 修改templates/pod.podspec中author字段、修改templates/Podfile中第4行为你自己的私有源地址
6. configPrivatePod目录下跑脚本配置Repo
7. 处理category工程，执行pod install
8. 处理业务工程，执行pod install
9. 测试主项目内引用本地category工程，podfile中添加本地pod：pod "本地pod", :path => "../pod目录"
10. 初始化fastlane
11. 使用项目根目录中的Fastfile替换fastlane/Fastfile文件、由于使用了cocoapods，需要在Gemfile文件中添加一行 gem "cocoapods"
12. 执行faslane 

关于步骤7、8、9请查看[在现有工程中实施基于CTMediator的组件化方案](https://casatwy.com/modulization_in_action.html)
