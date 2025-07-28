# K8S项目环境准备指南

## 基本要求

- **Go版本**: 1.21或更高版本
- **Git版本**: 2.0或更高版本
- **网络**: 能够访问GitHub

## 环境搭建

### 1. 克隆K8S项目
```bash
git clone https://github.com/kubernetes/kubernetes.git
cd kubernetes
```

### 2. 还原到测试状态

在进行代码测试前，需要将代码库还原到目标PR合并前的状态，以便验证修复效果。

#### 步骤说明：

1. **查看PR信息**
   ```bash
   git show <目标PR的Commit ID>
   ```
   此命令会显示PR的详细信息，包括：
   - 修改的文件列表
   - 具体的代码变更
   - merge字段中的两个ID（父提交ID和合并提交ID）

2. **还原到基线状态**
   ```bash
   git reset --hard <主干基线ID>
   ```
   使用主干基线ID（通常是merge字段中的第一个ID）将代码还原到PR合并前的状态。

3. **验证还原状态**
   ```bash
   git log --oneline -5
   ```
   检查当前HEAD是否指向正确的基线提交。

### 3. 多PR测试切换

当需要切换测试下一个PR时，使用目标PR的Commit ID直接切换：

```bash
# 1. 获取基线ID
git show <目标PR的Commit ID>

# 2. 切换到基线状态
git reset --hard <上一步输出的基线ID>
```
