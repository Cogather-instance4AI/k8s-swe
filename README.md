# K8S项目SWE评测案例集

本项目包含基于Kubernetes项目的软件工程评测案例，用于评估AI工具在K8S项目开发中的理解和代码修改能力。

## 项目结构

```
coding-testcase-k8s/
├── README.md                    # 项目说明文档
├── templates/                   # 用例模板
│   └── testcase_template.md    # 测试用例模板
├── testcases/                  # 具体测试用例
│   ├── bugfix_case/           # Bug修复类用例
│   │   └── case_133203/       # 异步抢占机制bug修复
│   └── feature_case/          # 功能开发类用例
│       └── case_133157/       # 特性功能实现
└── docs/                       # 文档
    └── environment_setup.md   # 环境准备指南
```

## 评测目标

每个测试用例包含两个主要评测维度：

1. **代码理解能力**：基于PR需求信息，让AI工具识别需要修改的代码文件和函数
2. **代码修改能力**：基于具体需求和代码片段，让AI工具进行准确的代码修改

## 用例结构

每个测试用例包含以下部分：
- PR详细信息（标题、编号、描述、变更统计、Git节点）
- 代码理解测试用例（Prompt、期望输出、参考答案）
- 代码修改测试用例（Prompt、期望输出、参考答案）

## 快速开始

### 1. 环境准备
```bash
# 克隆K8S项目
git clone https://github.com/kubernetes/kubernetes.git
cd kubernetes
```

### 2. 选择用例
- 查看 `testcases/` 目录下的具体用例
- 根据用例中的commit hash还原到测试状态

### 3. 执行测试
- 使用用例中的Prompt进行代码理解测试
- 使用用例中的Prompt进行代码修改测试
- 对比参考答案评估结果

## 现有测试用例

### Bug修复类用例
- **case_133203**: 异步抢占机制中的边界情况处理bug修复
  - 涉及调度器异步抢占逻辑的回滚操作
  - 难度：中等

### 功能开发类用例  
- **case_133157**: 特性功能实现
  - 涉及Kubernetes核心功能开发
  - 难度：中等

## 使用方法

1. 查看 `docs/environment_setup.md` 了解环境准备
2. 查看 `templates/testcase_template.md` 了解用例格式
3. 选择具体的测试用例进行评测

## 贡献指南

欢迎贡献新的测试用例，请遵循模板格式并确保用例的完整性和准确性。 