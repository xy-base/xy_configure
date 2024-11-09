<!--
 * @Author: yuyangit yuyangit.0515@qq.com
 * @Date: 2024-10-19 10:55:02
 * @LastEditors: yuyangit yuyangit.0515@qq.com
 * @LastEditTime: 2024-10-19 11:04:20
 * @FilePath: /xy_configure/README.md
 * @Description: 这是默认设置,请设置`customMade`, 打开koroFileHeader查看配置 进行设置: https://github.com/OBKoro1/koro1FileHeader/wiki/%E9%85%8D%E7%BD%AE
-->
# xy_configure

- [简体中文](./README.md)
- [繁體中文](./README.zh-hant.md)
- [English](./README.en.md)

## 说明

通用配置模块.


## 源码仓库

- <a href="https://github.com/xy-base/xy_configure.git" target="_blank">Github地址</a>  
- <a href="https://gitee.com/xy-opensource/xy_configure.git" target="_blank">Gitee地址</a>  
- <a href="https://gitcode.com/xy-opensource/xy_configure.git" target="_blank">GitCode地址</a>  

## 安装

```bash
# bash
pip install xy_configure
```

## 使用

```python
# Python Interpreter.
from xy_configure.Configure import Configure
from xy_configure.Pair.Section import Section
configure = Configure() 
configure['key_1'] = "value_1"
configure["key_2"] = "value_2"
print(configure)
# {"key_1":"value_1", "key_2":"value_2"}

configure = Configure() 
section = Section()
section.set_value("key_1","value_1")
configure.set_section(section)
print(configure)
# {'SECTION': {'key_1': 'value_1'}}
section.set_name("section_1")
configure.set_section(section)
print(configure)
# {'SECTION': {'key_1': 'value_1'}, 'section_1': {'key_1': 'value_1'}}
configure.del_section("SECTION")
print(configure)
# {'section_1': {'key_1': 'value_1'}}

```

## 许可证
xy_configure 根据 <木兰宽松许可证, 第2版> 获得许可。有关详细信息，请参阅 [LICENSE](LICENSE) 文件。


## 捐赠

如果小伙伴们觉得这些工具还不错的话，能否请咱喝一杯咖啡呢?  

![Pay-Total](./readme/Pay-Total.png)


## 联系方式

```
微信: yuyangiit
邮箱: yuyangit.0515@qq.com
```