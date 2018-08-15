# biz-jvm-invocation-sample
按照以下步骤执行 sample

cd biz-jvm-invocation-sample/facade && mvn clean install 在 facade 应用根目录中执行 mvn clean install 命令，把 facade 包安装到本地 maven 仓库，以便在 app-one 和 app-two 中添加 facade 依赖：

cd biz-jvm-invocation-sample/app-one && mvn clean package 在 app-one 应用根目录中执行 mvn clean package 命令，将应用打包成 Ark 包和 Biz 包，文件将输出到 biz-jvm-invocation-sample/app-one/target 目录

cd biz-jvm-invocation-sample/app-two && mvn clean package 在 app-two 应用根目录中执行 mvn clean package 命令，将应用打包成 Ark 包和 Biz 包，文件将输出到 biz-jvm-invocation-sample/app-two/target 目录

使用 java -jar 启动 app-one 应用的 Ark 包

使用 telnet localhost 1234 进入 Jarslink2.0 指令交互界面，并执行 install -b 指令，安装启动 app-two 的 Biz 包。

