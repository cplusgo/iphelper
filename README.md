# iphelper
在数据库的表设计时，
通常会保存下用户的ip地址，
用来检查用户操作合法性，
用一个整形就可以保存下，节省空间，提高检索速度。
Ip地址int string互转

可以通过下面两种方式使用

1.go get github.com/cplusgo/iphelper

2.govendor fetch github.com/cplusgo/iphelper
    
    

    package main
    
    
    import (
            "fmt"
            "github.com/cplusgo/iphelper"
    )
    
    
    func main() {
            ipStr := "127.0.0.1"
            ipInt := iphelper.StringIpToInt(ipStr)
            fmt.Println(ipInt)
            ipStr = iphelper.IntIpToString(ipInt)
            fmt.Println(ipStr)
    }