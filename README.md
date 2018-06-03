# GO 语言

GO语言是一门编译型语言

编译型语言和解释型语言的差异：
编译：在程序执行之前，有一个单独的编译过程，将程序翻译成机器语言就不用再进行翻译了
解释：是在运行的时候将程序翻译成机器语言
（比喻）：编译：做好一桌子菜在开吃
    解释：煮火锅边煮边吃，所以速度会比编译慢，因为边煮边吃

首先要部署环境
 
命令行工具：
go build 文件名.go   | 运行源码文件
go  run 文件名.go     | 编译且运行
go get  文件路径地址   | 获取远程代码包
工具使用：goLand专门为go语言的编辑器

go语言适合做什么？
Go语言主要用作服务器端开发，其定位是用来开发“大型软件”的，适合于很多程序员一起开发大型软件，并且开发周期长，支持云计算的网络服务。Go语言能够让程序员快速开发，并且在软件不断的增长过程中，它能让程序员更容易地进行维护和修改。它融合了传统编译型语言的高效性和脚本语言的易用性和富于表达性。

Go语言作为服务器编程语言，很适合处理日志、数据打包、虚拟机处理、文件系统、分布式系统、数据库代理等；网络编程方面，Go语言广泛应用于Web应用、API应用、下载应用等；除此之外，Go语言还可用于内存数据库和云平台领域，目前国外很多云平台都是采用Go开发。


Go语言成功案例：
Nsq：Nsq 是由Go语言开发的高性能、高可用消息队列系统，性能非常高，每天能处理数十亿条的消息；
Docker:基于lxc的一个虚拟打包工具，能够实现PAAS平台的组建。
Packer:用来生成不同平台的镜像文件，例如VM、vbox、AWS等，作者是vagrant的作者
Skynet：分布式调度框架
Doozer：分布式同步工具，类似ZooKeeper
Heka：mazila开源的日志处理系统
Cbfs：couchbase开源的分布式文件系统
Tsuru：开源的PAAS平台，和SAE实现的功能一模一样
Groupcache：memcahe作者写的用于Google下载系统的缓存系统
God：类似redis的缓存系统，但是支持分布式和扩展性
Gor：网络流量抓包和重放工具
Go语言作为一门大型项目开发语言，在很多大公司相继使用，甚至完全转向Go开发，其中代表有Google、Facebook、腾讯、百度、阿里巴巴、京东、小米以及360、美团、滴滴以及新浪等，因此，Go语言的开发前景还是很不错的！


文件结构：
package main  //程序所属包

import "fmt" //导入依赖包
 
const NAME = "imooc" //定义常量

var mainName = "main name"  //全局变量

type  imooc int //一般类型的声明

type  Learn  struct{}    //结构的声明

type  llearn interface{}  //声明接口

func  learnImooc(){    //函数定义
fmt.Print(" learnImooc ")
}

func main(){    //main()函数
}


func main(){
	fmt.Println("hello world!")
	fmt.Println(mainName)
	fmt.Println(NAME)
}

package:
 	package是最基本的分发单位和工程管理依赖关系的体现
每个GO语言源代码文件开头都是用友一个package声明，表示源代码文件所属代码包
要生成GO语言可执行程序，必须要有main的package包，且必须在该包下有main()函数
        同一个路径下只能存在一个package，一个package可以拆分成多个源文件组成

import：
import语句可以导入源代码文件所依赖的package包
不得导入源代码文件中没有用到的package，否则GO语言编译器会报错
import语法格式有两种：
第一种：
import “package1”
import “package2”
import “package2”
...
第二种：
import (
"package1"
      “package2”
      “package2”
...
)

import别名“.”  "_"
1、别名含义是：将导入的包命名为另一个容易记忆的别名
2、点（.）小做的含义是：点（.）标识的包导入后，调用该包中函数时可以省略前缀包名
3、下划线（_）操作的含义是：导入该包，但不导入整个包，而是执行该包中的init函数，因此无法通过包名来调用包中其他函数，使用下划线（_）操作往往是为了注册包里的引擎，让外部可以方便的使用。

Go语言 数据类型
整型，浮点型，复数，字符串，布尔型




