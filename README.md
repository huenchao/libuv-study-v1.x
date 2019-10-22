### 看libuv的源码的几个前置背景

1. 看官网给的图片，你会发现IO部分占了很大的比重，所以你需要先去了解一点[Linux IO](https://segmentfault.com/a/1190000003063859)相关知识。![](https://camo.githubusercontent.com/366d5cc03209320873f088d8a6ade73abf62ffbc/687474703a2f2f646f63732e6c696275762e6f72672f656e2f76312e782f5f696d616765732f6172636869746563747572652e706e67)
2. 会debug代码，直接照着这个[issue](https://github.com/huenchao/libuv-study-v1.x/issues/6)配置环境就行。
3. 一定要熟背uv_handle_s,uv_loop_s这两个结构体，你可以先拿timer、idle、check、prepare这些阶段的代码去debug，就会明白他的重要性。这些issue里都给了参考文章。
4. 当你把上面3件事情做的差不多了，准备看io_poll还有线程池的时候，可以看下这个视频[视频](https://www.youtube.com/watch?v=sGTRmPiXD4Y),他对network 1o架构和fs io架构在4:20的时候就开始说了。

