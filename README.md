# Excel2Unity
一个为Unity3D编写的插件，可以快速地将Excel文件转换为JSON、CSV和XML，方便在游戏过程中处理各种Excel文件。本项目参考了[excel2json](https://github.com/neil3d/excel2json)，在此表示感谢。

# 如何使用Excel2Unity
将本项目中的Source文件夹直接复制到Unity3D项目中即可，Unity3D的菜单栏将会增加一个Plugins的菜单项，通过此菜单项的ExcelTools打开插件窗口。在项目资源中选中Excel文件后，点击插件窗口上的"转换"按钮即可！

# 使用Excel2Unity的默认约束条件
* Excel数据表默认以第一行作为字段
* Excel工作表默认以第一个工作表为主
* 目前支持utf-8和gb2312两种字符编码类型

# 怎么解决Excel2Unity中的Bug？
* 提交[issues](https://github.com/qinyuanpei/Excel2Unity/issues)，然后由我来修改
* 因为编辑器插件的代码已经给出，所以如果你在使过程中遇到任何不爽的地方，可以直接修改源代码。

# Excel文件转换示例
假设Excel文件定义如下：
![Excel](http://7wy477.com1.z0.glb.clouddn.com/imgs_excel.png)
则经过转换后的JSON、CSV和Xml文件分别如下：
```JSON
[
  {
    "姓名": "李逍遥",
    "等级": 12.0,
    "描述": "《仙剑奇侠传1》男主角",
    "技能": "万剑诀",
    "登场时间": "仙剑1、仙剑2、仙剑5、仙剑5前传"
  },
  {
    "姓名": "慕容紫英",
    "等级": 20.0,
    "描述": "《仙剑奇侠传4》男主角",
    "技能": "千方残光剑",
    "登场时间": "仙剑4"
  },
  {
    "姓名": "夏侯瑾轩",
    "等级": 18.0,
    "描述": "《仙剑奇侠传5前传》男主角",
    "技能": "文星耀太虚",
    "登场时间": "仙剑5前传"
  },
  {
    "姓名": "皇甫卓",
    "等级": 24.0,
    "描述": "《仙剑奇侠传5前传》配角",
    "技能": "天中剑",
    "登场时间": "仙剑5前传"
  }
]
```

```CSV
姓名,等级,描述,技能,登场时间,
李逍遥,12,《仙剑奇侠传1》男主角,万剑诀,仙剑1、仙剑2、仙剑5、仙剑5前传,
慕容紫英,20,《仙剑奇侠传4》男主角,千方残光剑,仙剑4,
夏侯瑾轩,18,《仙剑奇侠传5前传》男主角,文星耀太虚,仙剑5前传,
皇甫卓,24,《仙剑奇侠传5前传》配角,天中剑,仙剑5前传,

```

```Xml
<?xml version="1.0" encoding="utf-8"?>
<Table>
  <Row>
   <姓名>李逍遥</姓名>
   <等级>12</等级>
   <描述>《仙剑奇侠传1》男主角</描述>
   <技能>万剑诀</技能>
   <登场时间>仙剑1、仙剑2、仙剑5、仙剑5前传</登场时间>
  </Row>
  <Row>
   <姓名>慕容紫英</姓名>
   <等级>20</等级>
   <描述>《仙剑奇侠传4》男主角</描述>
   <技能>千方残光剑</技能>
   <登场时间>仙剑4</登场时间>
  </Row>
  <Row>
   <姓名>夏侯瑾轩</姓名>
   <等级>18</等级>
   <描述>《仙剑奇侠传5前传》男主角</描述>
   <技能>文星耀太虚</技能>
   <登场时间>仙剑5前传</登场时间>
  </Row>
  <Row>
   <姓名>皇甫卓</姓名>
   <等级>24</等级>
   <描述>《仙剑奇侠传5前传》配角</描述>
   <技能>天中剑</技能>
   <登场时间>仙剑5前传</登场时间>
  </Row>
</Table>
```
