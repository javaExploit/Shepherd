# 关于执行指令收fee的问题

## 目的
- 防止有人发送无效TX, 通过收费使其付出代价
- 用价格调节网络业务量, 用的人多费用高，用的人少费用低
- 付的费用高的TX优先处理，

## 假设前提
- 出块节点获得的报酬 -> 代表了出块节点付出的劳动, 现在为1个SYS
- fee应该和出块节点付出的劳动相关，比如10%
- 最大出块速率20TX/秒，10秒钟-> 200TX (块内的最多的TX数量)
- (1 SYS/MAX_TX)*(当前需要打包的TX数量)*10%
- 最低fee 5%
- 最高fee 25%
- 动态的还是静态的比例?

## 出块节点的报酬
- 应该是和整体SYS量的年增幅相关，比如 总量*10%/每年, 允许的通货膨胀
- SYS初期发行量应该和链上需要跑的业务总量的价值相关
