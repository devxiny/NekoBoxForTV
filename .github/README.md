# 简介
原版没有适配TV，因此在原版的基础上增加了打开APP自动导入代理链接以及需要代理的APP包名，然后自动启动代理，这样不需要任何操作，直接点一下就可在TV上畅享。
# 说明
找到"ConfigurationFragment.kt"文件，下方代码位置，填充PROXY_LINK和PROXY_PACKAGE_LIST，打包编译成APK签名安装即可。
```
companion object {
    //代理链接
    private const val PROXY_LINK = ""
    //需要代理应用的包名
    private val PROXY_PACKAGE_LIST = listOf<String>()
}
```
参考配置
```
companion object {
    //一个Hysteria2的代理链接
    private const val PROXY_LINK = "hy2://1234568@25.25.36.21:10086?insecure=1&sni=www.xxx.com#Abc-Hysteria2"
    //SmartTube正式版和测试版包名
    private val PROXY_PACKAGE_LIST = listOf<String>("com.teamsmart.videomanager.tv","com.liskovsoft.smarttubetv.beta")
}
```
# 感谢
https://github.com/MatsuriDayo/NekoBoxForAndroid