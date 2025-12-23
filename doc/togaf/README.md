# Node.js TOGAF Enterprise Architecture Diagrams

本目录包含基于TOGAF（The Open Group Architecture Framework）框架的Node.js企业架构图，采用PlantUML格式。

## 目录结构

```
doc/togaf/
├── README.md
├── zh/                    # 中文版架构图
│   ├── business-architecture.puml
│   ├── application-architecture.puml
│   ├── data-architecture.puml
│   └── technology-architecture.puml
└── en/                    # 英文版架构图
    ├── business-architecture-en.puml
    ├── application-architecture-en.puml
    ├── data-architecture-en.puml
    └── technology-architecture-en.puml
```

## 架构图说明

### 1. 业务架构图 (Business Architecture)

**文件位置：**
- 中文版：`zh/business-architecture.puml`
- 英文版：`en/business-architecture-en.puml`

**内容概述：**
- **业务能力层**：JavaScript运行时服务、包管理生态系统、开发者社区支持、跨平台支持能力
- **业务流程层**：应用开发流程、包发布流程、问题处理流程、版本发布流程
- **业务角色层**：开发者、维护者、TSC技术委员会、协作者、问题分类员、发布团队
- **业务价值层**：跨平台JavaScript执行、生态系统支持、长期维护保障、开放治理模式

### 2. 应用架构图 (Application Architecture)

**文件位置：**
- 中文版：`zh/application-architecture.puml`
- 英文版：`en/application-architecture-en.puml`

**内容概述：**
- **应用接口层**：HTTP/HTTPS、文件系统、加密、流处理、网络、进程管理等模块
- **核心应用层**：模块系统（CommonJS/ESM）、事件系统、异步钩子、缓冲区管理等
- **应用服务层**：DNS、TLS/SSL、子进程管理、REPL、调试器、性能监控、测试框架
- **应用集成层**：N-API接口、原生插件、Web API兼容、WASI支持

### 3. 数据架构图 (Data Architecture)

**文件位置：**
- 中文版：`zh/data-architecture.puml`
- 英文版：`en/data-architecture-en.puml`

**内容概述：**
- **数据源层**：JavaScript源代码、C++绑定代码、配置文件、包元数据
- **数据实体层**：代码数据、配置数据、运行时数据、元数据
- **数据流层**：模块加载流程、数据序列化、流处理管道、数据转换
- **数据存储层**：文件系统、内存管理、缓存机制、快照存储

### 4. 技术架构图 (Technology Architecture)

**文件位置：**
- 中文版：`zh/technology-architecture.puml`
- 英文版：`en/technology-architecture-en.puml`

**内容概述：**
- **应用技术层**：Node.js核心、JavaScript API、内置模块
- **运行时技术层**：V8 JavaScript引擎、libuv事件循环、N-API绑定层
- **系统技术层**：操作系统接口（Linux/Windows/macOS）、网络协议栈、文件系统接口
- **基础设施层**：构建系统（GYP/GN/CMake）、测试框架、CI/CD系统
- **技术标准层**：ECMAScript、HTTP、TLS、Web标准

## 如何使用

### 渲染PlantUML图表

这些`.puml`文件可以使用多种方式渲染为图片：

#### 方法1：使用PlantUML在线服务器

1. 访问 [PlantUML在线服务器](http://www.plantuml.com/plantuml/uml/)
2. 复制`.puml`文件内容
3. 粘贴到编辑器中
4. 点击"Submit"生成图表

#### 方法2：使用本地PlantUML工具

**安装PlantUML：**

```bash
# 使用npm安装
npm install -g node-plantuml

# 或使用Java（需要先安装Java）
# 下载plantuml.jar
wget http://sourceforge.net/projects/plantuml/files/plantuml.jar/download -O plantuml.jar
```

**渲染图表：**

```bash
# 使用node-plantuml
puml generate zh/business-architecture.puml -o output.png

# 或使用Java
java -jar plantuml.jar zh/business-architecture.puml
```

#### 方法3：使用VS Code扩展

1. 在VS Code中安装"PlantUML"扩展
2. 打开`.puml`文件
3. 按`Alt+D`（Windows/Linux）或`Option+D`（macOS）预览图表
4. 右键点击图表可以导出为PNG、SVG等格式

#### 方法4：使用IntelliJ IDEA / WebStorm

1. 安装PlantUML插件
2. 打开`.puml`文件
3. 右键选择"PlantUML" -> "Preview Diagram"
4. 可以导出为各种格式

### 编辑架构图

所有架构图使用标准的PlantUML语法，可以直接编辑`.puml`文件来修改架构图内容。

**主要语法元素：**
- `package`：定义包/层
- `[组件名称] as 别名`：定义组件
- `-->`：定义组件间的关系
- `note right of 组件`：添加注释说明

## 架构图关系

这四个架构图遵循TOGAF的四个核心架构域：

```
业务架构 → 应用架构 → 数据架构 → 技术架构
    ↓         ↓         ↓         ↓
业务需求  应用组件  数据实体  技术实现
```

- **业务架构**定义了业务能力和价值
- **应用架构**定义了应用组件和交互
- **数据架构**定义了数据实体和流程
- **技术架构**定义了技术组件和标准

## 更新说明

这些架构图基于Node.js项目的实际结构（`src/`、`lib/`、`deps/`等目录）创建，反映了Node.js的核心架构设计。

如需更新架构图以反映Node.js的新功能或架构变化，请：
1. 编辑相应的`.puml`文件
2. 保持中英文版本同步
3. 更新本README文件中的相关说明

## 参考资源

- [TOGAF官方文档](https://www.opengroup.org/togaf)
- [PlantUML官方文档](https://plantuml.com/)
- [Node.js官方文档](https://nodejs.org/docs/)

## 贡献

欢迎提交Pull Request来改进这些架构图。在提交前，请确保：
- 中英文版本保持同步
- PlantUML语法正确
- 架构图内容准确反映Node.js的实际架构

