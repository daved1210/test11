# 待办事项应用 - 多人协作版

## 架构

- **前端**: 纯 HTML/CSS/JS 单页应用
- **后端**: Node.js + Express
- **数据存储**: JSON 文件 (tasks.json)
- **实时同步**: 轮询机制 (每2秒刷新)

## API 接口

| 方法 | 路径 | 描述 |
|------|------|------|
| GET | /api/tasks | 获取所有任务 |
| POST | /api/tasks | 创建新任务 |
| PUT | /api/tasks/:id | 更新任务 |
| DELETE | /api/tasks/:id | 删除任务 |

## 数据模型

```json
{
  "id": "string",
  "text": "string",
  "priority": "high | medium | low",
  "completed": boolean,
  "createdAt": timestamp
}
```

## 运行方式

```bash
npm install
npm start
# 访问 http://localhost:3000
```

## 部署

- 可使用 PM2 或 Docker 部署
- 支持多进程处理并发请求
- JSON 文件会自动备份
