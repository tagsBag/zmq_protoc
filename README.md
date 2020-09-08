# zmq
## 1.libzmq
  下载:https://zeromq.org/download/
	libzmq-v141-x64-4_3_2.zip
	包含:
		1.libzmq-v141-mt-4_3_2.lib
		2.libzmq-v141-mt-4_3_2.dll
		3.zmq.h
	  引用1,2做库,main.cpp中包含zmq.h即可运行
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
	
	
4.zmq+protoc
	1.c++ protoc
		protoc -I ./ --cpp_out=. msg.proto
		将在当前目录生成两文件:
			1.msg.pb.cc
			2.msg.pb.h
