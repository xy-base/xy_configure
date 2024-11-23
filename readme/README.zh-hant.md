# xy_configure

| [简体中文](../README.md)         | [繁體中文](./README.zh-hant.md)        |                      [English](./README.en.md)          |
| ----------- | -------------|---------------------------------------|

## 說明

通用配置模組.

## 程式碼庫

| [Github](https://github.com/xy-base/xy_configure.git)         | [Gitee](https://gitee.com/xy-opensource/xy_configure.git)        |                      [GitCode](https://gitcode.com/xy-opensource/xy_configure.git)          |
| ----------- | -------------|---------------------------------------|


## 安裝

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

## 許可證
xy_configure 根據 <木蘭寬鬆許可證, 第2版> 獲得許可。有關詳細信息，請參閱 [LICENSE](../LICENSE) 文件。

## 捐贈

如果小夥伴們覺得這些工具還不錯的話，能否請咱喝一杯咖啡呢?  
![pay-total](./pay-total.png)

## 聯繫方式

微信: yuyangiit
郵箱: yuyangit.0515@qq.com
```