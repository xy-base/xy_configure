# xy_configure

| [简体中文](../README.md)         | [繁體中文](./README.zh-hant.md)        |                      [English](./README.en.md)          |
| ----------- | -------------|---------------------------------------|

## Description

Generic configuration module.


## Source Code Repositories

| [Github](https://github.com/xy-base/xy_configure.git)         | [Gitee](https://gitee.com/xy-opensource/xy_configure.git)        |                      [GitCode](https://gitcode.com/xy-opensource/xy_configure.git)          |
| ----------- | -------------|---------------------------------------|


## Installation

```bash
# bash
pip install xy_configure
```

## How to use

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

## License
xy_configure is licensed under the <Mulan Permissive Software License，Version 2>. See the [LICENSE](../LICENSE) file for more info.

## Donate

If you think these tools are pretty good, Can you please have a cup of coffee?  

![Pay-Total](./Pay-Total.png)  


## Contact

```
WeChat: yuyangiit
Mail: yuyangit.0515@qq.com
```