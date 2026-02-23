# Medi-Hub 医药管理系统

[![Spring Boot](https://img.shields.io/badge/Spring%20Boot-2.7.18-brightgreen)](https://spring.io/projects/spring-boot)
[![Vue](https://img.shields.io/badge/Vue-3.4.0-4fc08d)](https://vuejs.org/)
[![MySQL](https://img.shields.io/badge/MySQL-8.0-4479a1)](https://www.mysql.com/)

Medi-Hub 是一款功能完善的医药管理系统，为药房、医院药品管理部门提供药品库存管理、销售订单处理、物流追踪及数据分析等一站式解决方案。
视频介绍：https://www.bilibili.com/video/BV1uJfcBvEXC/?share_source=copy_web&vd_source=bf386503a362c98932b627e6f7ac015e
需要联系QQ:1150884107
## 功能截图
<img width="1040" height="472" alt="e7bff3b8bdf9c3d163fbb892e2b4cd9a" src="https://github.com/user-attachments/assets/a05654a5-44fc-44ca-987c-e956185a367a" />

<img width="1007" height="497" alt="3536edde439344e95c5079ae5b5d419a" src="https://github.com/user-attachments/assets/8b089b9f-2dd7-4c1e-a248-4babee585768" />

<img width="1664" height="790" alt="d8522fce1e0fa19f191928db4a77c146" src="https://github.com/user-attachments/assets/38484703-9917-403c-b93e-76743edd9f7b" />

<img width="1586" height="820" alt="68198d5c75aa2dc26fb375781393da5a" src="https://github.com/user-attachments/assets/5b5e0da0-6fef-4d13-8d09-3e4c575de8f7" />

<img width="1625" height="871" alt="5434af15734da4753cbf605d707299f7" src="https://github.com/user-attachments/assets/969f07be-7f7b-4ef3-a967-a0eef6c054f8" />

<img width="1700" height="765" alt="30bd93f9d8c9f502349a66f82777e169" src="https://github.com/user-attachments/assets/4127dc00-5f12-4419-907a-c8db386afdae" />

<img width="1699" height="779" alt="c7662dc6999864149ba20fc0beb5fca7" src="https://github.com/user-attachments/assets/37d43536-fc65-4317-b420-20d5d4fb23a4" />

<img width="1608" height="826" alt="e1eefca1cc5a1c7e9da0542d263a8fb2" src="https://github.com/user-attachments/assets/d50542d0-f4c2-433f-8ef6-cd1f6bc009b6" />

## 功能特性

### 用户管理
- 多角色权限控制（管理员/员工/普通用户）
- 用户注册、登录认证
- JWT Token 安全会话管理

### 药品管理
- 药品信息增删改查
- 药品分类（中药/西药/保健品）
- 库存预警提醒

### 库存管理
- 出入库记录管理
- 库存实时监控
- 低库存预警

### 销售管理
- 购药订单处理
- 取药/退药记录
- 订单状态流转

### 物流管理
- 物流信息追踪
- 配送状态更新
- 收货人信息管理

### 公告系统
- 系统公告发布
- 公告置顶功能

### 数据分析
- 销售数据统计
- 库存数据分析
- 可视化图表展示

## 技术栈

| 层级 | 技术 | 版本 |
|------|------|------|
| 后端框架 | Spring Boot | 2.7.18 |
| 持久层 | MyBatis | 2.3.2 |
| 认证 | java-jwt | 4.4.0 |
| 数据库 | MySQL | 8.0 |
| 前端框架 | Vue | 3.4.0 |
| 构建工具 | Vite | 5.4.0 |
| 状态管理 | Pinia | 2.1.0 |
| UI 组件 | Element Plus | 2.7.0 |
| 图表 | ECharts | 6.0.0 |

## 项目结构

```
medi-hub/
├── backend/                          # 后端服务
│   └── src/main/java/com/medihub/
│       ├── controller/               # REST API 控制器
│       ├── service/                  # 业务逻辑层
│       ├── mapper/                   # MyBatis Mapper
│       ├── entity/                   # 数据实体
│       ├── common/                   # 公共组件
│       ├── config/                   # 配置类
│       ├── interceptor/              # 拦截器
│       └── exception/                # 异常处理
├── frontend/                         # 前端应用
│   └── src/
│       ├── views/                    # 页面组件
│       ├── api/                      # API 请求模块
│       ├── router/                   # 路由配置
│       ├── store/                    # 状态管理
│       ├── components/               # 公共组件
│       ├── styles/                   # 样式文件
│       └── utils/                    # 工具函数
└── sql/                              # 数据库脚本
    └── init.sql                      # 初始化 SQL
```

## 快速开始

### 环境要求
- JDK 1.8+
- Maven 3.6+
- Node.js 16+
- MySQL 8.0+

### 启动步骤

1. **初始化数据库**
   ```bash
   mysql -u root -p < sql/init.sql
   ```

2. **启动后端服务**
   ```bash
   cd backend
   mvn spring-boot:run
   ```

3. **启动前端应用**
   ```bash
   cd frontend
   npm install
   npm run dev
   ```

4. **访问系统**
   - 前端地址：http://localhost:5173
   - 后端 API：http://localhost:8088/api

详细安装配置请参考 [QUICKSTART.md](QUICKSTART.md)

## API 概览

| 模块 | 路径 | 说明 |
|------|------|------|
| 认证 | `/api/auth` | 登录、注册、验证码 |
| 用户 | `/api/user` | 用户管理 CRUD |
| 药品 | `/api/medicine` | 药品信息管理 |
| 取退记录 | `/api/medicine-record` | 取药/退药记录 |
| 订单 | `/api/order` | 购药订单管理 |
| 库存 | `/api/stock-record` | 出入库记录 |
| 库存预警 | `/api/inventory` | 库存预警查询 |
| 物流 | `/api/logistics` | 物流信息管理 |
| 公告 | `/api/announcement` | 系统公告 |
| 数据分析 | `/api/data-analysis` | 统计图表数据 |

## 用户角色权限

| 角色 | 权限范围 |
|------|----------|
| **ADMIN** | 全部功能，包括用户管理、员工管理、数据分析 |
| **EMPLOYEE** | 药品管理、库存管理、订单处理、物流管理 |
| **USER** | 公告查看、个人中心、物流追踪、我的订单 |

## 默认账号

| 角色 | 用户名 | 密码 |
|------|--------|------|
| 管理员 | admin | admin123 |

新用户默认密码：`123456`

## 数据库表

| 表名 | 说明 |
|------|------|
| sys_user | 系统用户表 |
| sys_log | 操作日志表 |
| medicine | 药品信息表 |
| medicine_record | 药品取退记录表 |
| medicine_order | 购药订单表 |
| stock_record | 出入库记录表 |
| logistics | 物流信息表 |
| announcement | 公告表 |

## 系统架构文档

使用支持 Mermaid 的工具打开文档即可渲染所有图表：

- Typora（推荐）

- VS Code + Mermaid 插件
- GitHub/GitLab 在线预览
-  IntelliJ IDEA + Markdown插件

[>>系统架构文档](docs/SYSTEM_ARCHITECTURE.md)

源码QQ:1150884107
