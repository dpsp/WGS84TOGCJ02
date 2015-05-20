# WGS84TOGCJ02
/*
WGS-84 坐标系，是GPS系统所采用的坐标系，一切正常工作的GPS或GPS芯片所返回的坐标值都是这个坐标系下的数值，
Google地图采用的卫星图也是按照这坐标系摆放的。
GCJ-02 坐标系，是我天朝政府搞出来的加密坐标系，也常常被称为 “火星坐标系”。
包括（但可能不限于）高德地图在内的国内地图服务商采用它来绘制地图。
Apple、  *  Google 等国外公司在其道路地图中使用的也是高德的数据。
BD-09 坐标系则是百度地图专用的坐标系。 
*/

可以使用如下方法，预先判断是否是中国位置
+ (BOOL)isLocationOutOfChina:(CLLocationCoordinate2D)location {
    if (location.longitude < 72.004 || location.longitude > 137.8347 || location.latitude < 0.8293 || location.latitude > 55.8271)
        return YES;
    return NO;
}

