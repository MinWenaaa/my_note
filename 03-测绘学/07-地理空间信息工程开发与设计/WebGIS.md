# 二、WebGIS的主要产品和技术
## WebGIS的技术基础和基本架构
- 超文本传输协议（HTTP）
- 超文本标记语言（HTML）
- 通义资源定位器（URL）
## WebGIS的部署方式
- 公有云模式：ArcGIS Online
- 混合模式
- 私有云模式：ArcGIS Enterprise

# 三、Web服务
### WMS（Web地图服务）
- GetCapabitities：返回服务元数据
- GetMap：
- GetFeatureInfo：
- GetLegendGraphic：
### WMTS（Web地图瓦片服务）
提供静态数据
### WFS（Web要素服务）
对地理矢量要素进行插入、更新、删除、检索服务。支持基于空间几何关系的查询与基于属性域的查询
- GetCapabitities：
- DescribeFeatureType：
- GetFeature：
- LockFeature：
- Transaction：
### WCS（Web覆盖服务）
将包含地理位置的地理空间数据作为“覆盖”在网上相互交换。WMS返回的是失去原始值的图片，WCS有原始值。
- GetCapabitities：
- DescribeCoverage：
### WPS（Web处理服务）
在互联网上进行地理分析提供的服务
## Web应用的基本组成
### 基础底图
### 可操作图层
### 工具