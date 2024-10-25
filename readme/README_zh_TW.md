<!--
 * @Author: yuyangit yuyangit.0515@qq.com
 * @Date: 2024-10-19 10:54:58
 * @LastEditors: yuyangit yuyangit.0515@qq.com
 * @LastEditTime: 2024-10-19 11:08:12
 * @FilePath: /xy_configure/readme/README_zh_TW.md
 * @Description: 这是默认设置,请设置`customMade`, 打开koroFileHeader查看配置 进行设置: https://github.com/OBKoro1/koro1FileHeader/wiki/%E9%85%8D%E7%BD%AE
-->
# xy_configure

- [简体中文](README_zh_CN.md)
- [繁体中文](README_zh_TW.md)
- [English](README_en.md)

## 說明

通用配置模組.

## 程式碼庫

- <a href="https://github.com/xy-base/xy_configure.git" target="_blank">Github位址</a>  
- <a href="https://gitee.com/xy-base/xy_configure.git" target="_blank">Gitee位址</a>

## 安裝

```bash
pip install xy_configure
```

## 使用

###### python腳本

```python
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

## 許可證
xy_configure 根據 <木蘭寬鬆許可證, 第2版> 獲得許可。有關詳細信息，請參閱 [LICENSE](../LICENSE) 文件。

## 捐贈

如果小夥伴們覺得這些工具還不錯的話，能否請咱喝一杯咖啡呢?  

![Pay-Total](./Pay-Total.png)

## 聯繫方式

微信: yuyangiit
郵箱: yuyangit.0515@qq.com
```