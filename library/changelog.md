# gpslib.h 更新日志
作者：吉吉

## v1.2 2020年8月4日
* 修复 `char* getCode(double lat, double lon)` 部分区域会计算错误
* 优化 返回值由堆中动态分配

## v1.1 2020年1月28日
* 修复 `char* getCode(double lat, double lon)` 的野内存会导致字符串溢出的bug
* 兼容 51单片机 可直接包含本头文件
* 新增 RMC结构体
* 新增 解析RMC信息 `RMC rmc2data(char* str)`
* 完善 度分经纬度格式转换 `double degree2format(double value)` 的介绍
* 优化 `double* gps2data(char* str)` 的算法

## v1.0 2020年1月9日
* 新增 解析GPS芯片的经纬度 `double* gps2data(char* str)`
* 新增 通过经纬度获取梅登黑德格网编号 `char* getCode(double lat, double lon)`
* 注意 代码全部使用 `UTF-8` 编码，如有乱码请转为 `ANSI`