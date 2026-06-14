# solo-6600018: 古籍数字化 OCR 与标注平台

## 技术栈
- Frontend: Vue 3 + TypeScript + Vite + Pinia + Tailwind CSS + Canvas/SVG
- Backend: Python FastAPI + PaddleOCR (mock)

## 核心特性
1. **竖排古籍 OCR**：上传古籍图片，识别竖排繁体文字
2. **区域标注**：拖拽框选图片区域，添加章节/段落/异体字标注
3. **异体字对照**：繁体/异体字→简体自动转换对照字典
4. **全文检索**：跨文档全文搜索，高亮匹配结果
5. **TEI/XML 导出**：标注结果导出为 TEI 标准 XML 格式
6. **人工校正**：逐行 OCR 结果人工修正，置信度标注

## 快速开始（推荐：使用 Make 统一命令）

```bash
# 1. 安装所有依赖
make install

# 2. 同时启动前后端
make dev

# 3. 一键完整校验（类型检查 → 构建 → 接口健康检查）
make check-all
```

### 所有可用命令
```bash
make help          # 查看全部命令列表
make install       # 安装前后端所有依赖
make dev           # 同时启动前后端开发服务
make typecheck     # 前端 TypeScript 类型检查
make build-frontend # 前端生产构建检查
make health-check  # 后端接口健康检查
make check-all     # 完整流水线校验
make clean         # 清理构建产物
make stop          # 停止前后端服务
```

## 手动启动（不推荐）
```bash
# Frontend
cd frontend && npm install && npm run dev

# Backend
cd backend && pip install -r requirements.txt && uvicorn app.main:app --reload
```
