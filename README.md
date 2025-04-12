# JSON to TypeScript Interface Converter

![VSCode Version](https://img.shields.io/badge/VSCode-%3E%3D1.74.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)

一款智能将JSON对象转换为TypeScript接口的VSCode插件，支持嵌套对象处理和智能命名规范。
********
## ✨ 特性

- 🔄 ​**​一键转换​**​：快速将选中的JSON转换为TS接口
- 🧩 ​**​嵌套对象处理​**​：自动生成子级接口
- 🏷️ ​**​智能命名​**​：自动采用大驼峰命名规范（PascalCase）
- 📋 ​**​多格式支持​**​：完美处理数组、对象和基础类型
- ⚙️ ​**​配置选项​**​：支持自定义默认接口名称

## 📦 安装

1. 打开VSCode扩展面板 (`Ctrl+Shift+X`)
2. 搜索 `JSON to TS Interface`
3. 点击安装按钮

或通过命令行安装：
```bash
code --install-extension json-to-ts-interface.vsix
```
# 使用方式
1. 在JSON文件中选中需要转换的对象
2. 执行以下任一操作：
   1. 右键选择 `JSON替换Interface` / `JSON创建新Interface`
   2. 使用命令面板 (Ctrl+Shift+P) 执行 `JSON替换Interface` / `JSON创建新Interface`
3. 输入接口名称（可选）
4. 自动生成TS接口代码
   
​​输入 JSON​​:
``` json
{
  "user": {
    "firstName": "John",
    "lastName": "Doe",
    "addresses": [
      {
        "street": "Main St",
        "number": 123
      }
    ]
  }
}
```
​​生成 TypeScript​​:

```typescript
interface Address {
  street: string;
  number: number;
}

interface User {
  firstName: string;
  lastName: string;
  addresses: Address[];
}

interface Example {
  user: User;
}
```