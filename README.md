# zmq
## 1.libzmq
  	下载:https://zeromq.org/download/
	libzmq-v141-x64-4_3_2.zip
	包含:
		1.libzmq-v141-mt-4_3_2.lib
		2.libzmq-v141-mt-4_3_2.dll
		3.zmq.h
	引用1,2做库,main.cpp中包含zmq.h即可运行,看到的网上示例都是针对老版本libzmq的linux版本
    	是一个c语言写的库
## 2.cppzmq
	下载 https://github.com/zeromq/cppzmq
	包含:
		1.zmq.hpp
		2.zmq_addon.hpp
    	是对 libzmq 的 c++ 封装,依赖 libzmq
## 3.littleRpc
	https://github.com/tashaxing/LittleRpc
	更方便与 rpc 的对 cppzmq 的封装
    
## 4.说明:
	1.libzmq使zmq的实现,用c实现,下载的是与编译版本,所以无需编译
	2.cppzmq是对libzmq的一个c++包裹,方便以c++的方式调用	
	3.littleRpc是一个建立在 cppzmq 之上 的 rpc 实现,可以更加方便使用
	
# protoc
## 1.protoc
	protoc 是一个语言无关的,可以理解为同 xml,json类似的对数据进行格式化的东西,做好格式化之后,可以做任何事情,包括通过zmq在网络上传输
## 2.c++ protoc
	1.预编译版本protoc
		https://github.com/protocolbuffers/protobuf/releases/tag/v3.13.0
		protoc-3.13.0-win64.zip
		预编译版本protoc dll用-MT参数编译,引用工程也需要以此参数编译
			QMAKE_CXXFLAGS_RELEASE += -MT
			QMAKE_CFLAGS_RELEASE += -MT
	2.compilation with source
		
	protoc -I ./ --cpp_out=. msg.proto
	将在当前目录生成两文件:
		1.msg.pb.cc
		2.msg.pb.h
