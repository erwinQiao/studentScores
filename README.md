# Django 学生管理系统(学习记录)

本项目的目的用于学习**Django web**开发的完整构建过程，通过逐步实现一个简答的学生管理系统，理解Django的核心机制和开发流程

> 本项目为学习用途，功能逐步完善中，主要是空闲时间学习，不定期

## 学习目标

通过本项目，学习并掌握

- Django 项目与App的基本结构
- git 多分支开发的流程
- Django MTV架构思想
- Python的熟练
- URL路由，视图和模板的操作
- Django ORM的基本使用
- 表单处理与后台管理
- uv 工程管理思想
- 项目开发的流程

## 学习环境

- Python > 3.10
- Django 5.2.5
- 数据库：
- 操作系统：WSL2 Ubuntu 22.04/MacOS
- 编辑器：VSCode

## 学习路线

### 第一阶段 项目初始化

- uv 初始化及django软件安装和虚拟环境的搭建
- 创建Django项目
- 启动开发服务器

1. uv 初始化

```bash
# uv 创建目录，初始化项目
uv init

# uv 安装软件添加虚拟环境
uv add django

# uv pip install
uv pip install django==5.2.5

# 激活虚拟环境
source .venv/bin/activate

# 检验软件
django-admin --version

```

2. 启动Django项目

