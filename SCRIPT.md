# GMSV Avaritia Script Update

## 新增命令介绍

### 取值函数(用于BLOCK\IF等)

#### myplayer dataslot
说明： 获取玩家指定数据库栏位的值

语法演示： 

`BLOCK myplayer 9 == 1` -- 获取玩家等级，如果为1继续该Block

#### mypet petpos,dataslot
说明： 获取玩家指定位置宠物的数据库栏位的值，petpos取值为0-4，0表示第一只宠物

语法演示： 

`BLOCK mypet 0,9 == 1` -- 获取玩家的第一只宠物的等级，如果为1继续该Block

#### myitem itempos,dataslot
说明： 获取玩家指定位置道具的数据库栏位的值，itempos取值为0-27，0-7表示装备栏，8-27表示身上道具栏，注意：dataslot不同于宠物和人物，要从0开始计算

语法演示： 

`BLOCK myitem 8,0 == 9200` -- 获取玩家道具栏第一个道具的ID，如果为9200继续该Block

### 赋值函数

#### mysetplayer i,r,s,v
说明：同理小男生的万能脚本setmoonboydb，使用方式相同

i = 0/1 0:复写模式 1:增量模式

r 如果i为增量模式，此值将设定目标值的上限，当i为复写模式时，此值无效，-1即可

s 数据库栏位

v 给定的数值

语法演示：
`mysetplayer 1,-1,42,5000` -- 让玩家获取5000经验值

#### mysetpet p,i,r,s,v
说明：万能宠物脚本，设置宠物的数值型数据

p 宠物的位置，取值范围0-4 0表示第一个宠物

i = 0/1 0:复写模式 1:增量模式

r 如果i为增量模式，此值将设定目标值的上限，当i为复写模式时，此值无效，-1即可

s 数据库栏位

v 给定的数值

语法演示：
`mysetpet 0,1,-1,42,5000` -- 让玩家的第一个宠物获得5000经验

#### mysetitem p,i,r,s,v
说明：万能宠物脚本，设置宠物的数值型数据

p 物品的位置，取值范围0-27 0-7表示装备栏 8-27表示道具栏

i = 0/1 0:复写模式 1:增量模式

r 如果i为增量模式，此值将设定目标值的上限，当i为复写模式时，此值无效，-1即可

s 数据库栏位（从0开始计算）

v 给定的数值

语法演示：
`mysetitem 8,1,-1,9,1` -- 让玩家的道具栏的第一个道具堆叠数量增加一个


