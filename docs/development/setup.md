# 环境搭建

## 前置要求

- Debian 13 (trixie) 或兼容 Linux 发行版
- ARM64 (aarch64) 架构
- Python >= 3.10
- Node.js >= 18
- Git

## 克隆项目

```bash
git clone <仓库地址>
cd Passnux
```

## 后端环境

```bash
# 创建虚拟环境
python3 -m venv venv
source venv/bin/activate

# 安装依赖（待补充）
pip install -r requirements.txt
```

## 前端环境

```bash
# 安装依赖（待补充）
cd src/frontend
npm install
```

## 验证安装

```bash
# 检查 Python 版本
python3 --version

# 检查 Node.js 版本
node --version