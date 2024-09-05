# rpc<br>
## This project is a distributed rpc communication framework based on the muduo and protobuf libraries.<br>
查看注册中心是否成功运行，如果没有运行，则<br>
`cd zookeeper-3.4.12/bin`<br>
`./zkServer.sh start`<br>
一键编译方式<br>
`./autobuild.sh`<br>
服务端运行<br>
`cd bin/`<br>
`./provider -i test.conf`<br>
客户端运行<br>
`./consumer -i test.conf`
