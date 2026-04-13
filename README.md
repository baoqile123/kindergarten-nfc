# 🏫 幼儿园NFC签到系统 - GitHub Pages迁移指南

## 📋 迁移概述

将现有的户外运动NFC签到系统从freekit.dev迁移到GitHub Pages，解决部分地区访问不稳定的问题。

### 🔗 链接变化
- **旧链接**：`https://freekit.dev/s/ejyVDEKU`
- **新链接**：`https://[用户名].github.io/kindergarten-nfc/nfc-checkin.html`

### 🎯 迁移目标
1. ✅ 解决访问稳定性问题
2. ✅ 保持所有功能不变
3. ✅ 提供长期免费托管
4. ✅ 支持自定义域名

## 🚀 快速开始

### 第一步：创建GitHub仓库
1. 访问 https://github.com/new
2. 填写信息：
   - **Repository name**: `kindergarten-nfc`（建议）
   - **Public**: 公开仓库
   - **不要勾选**"Add a README file"
3. 点击"Create repository"

### 第二步：上传文件
1. 将本文件夹（`github_pages_deploy`）中的所有文件上传到仓库
2. 可以通过Web界面上传，或使用Git命令

### 第三步：启用GitHub Pages
1. 进入仓库：`https://github.com/[用户名]/kindergarten-nfc`
2. 点击"Settings"选项卡
3. 左侧选择"Pages"
4. 配置：
   - **Source**: Deploy from a branch
   - **Branch**: main，路径`/(root)`
5. 点击"Save"

### 第四步：等待部署
- 等待约1-3分钟
- 刷新页面查看状态（显示绿色✅即成功）

## 📱 访问地址

### 主页面
```
https://[用户名].github.io/kindergarten-nfc/nfc-checkin.html
```

### 6个运动区域专用链接
```
🏀 灌篮小乐宝：https://[用户名].github.io/kindergarten-nfc/nfc-checkin.html?area=灌篮小乐宝
💻 IT小乐宝：https://[用户名].github.io/kindergarten-nfc/nfc-checkin.html?area=IT小乐宝
🚗 智驾小乐宝：https://[用户名].github.io/kindergarten-nfc/nfc-checkin.html?area=智驾小乐宝
🎯 智酷小乐宝：https://[用户名].github.io/kindergarten-nfc/nfc-checkin.html?area=智酷小乐宝
🪢 绳趣小乐宝：https://[用户名].github.io/kindergarten-nfc/nfc-checkin.html?area=绳趣小乐宝
🧗 芯动小乐宝：https://[用户名].github.io/kindergarten-nfc/nfc-checkin.html?area=芯动小乐宝
```

### 手环链接模板
```
https://[用户名].github.io/kindergarten-nfc/nfc-checkin.html#姓名
```

## 🛠️ 文件结构

```
github_pages_deploy/
├── nfc-checkin.html          # 核心签到页面（完整功能）
├── index.html               # 欢迎页面（可选）
├── CNAME                    # 自定义域名配置（预留）
├── .nojekyll                # 禁用Jekyll处理
├── README.md                # 本文件
├── 迁移操作指南.pdf          # 详细操作步骤
├── deploy_script.py         # 自动化部署脚本
├── update_excel_links.py    # Excel链接更新脚本
└── 测试验证报告.md           # 功能验证结果
```

## 🔧 功能验证

### ✅ 已验证功能
1. **中文URL参数支持**：`?area=灌篮小乐宝#姓名`
2. **localStorage数据存储**：签到记录本地保存
3. **CSV导出功能**：按E键导出签到记录
4. **区域切换**：按A键切换6个运动区域
5. **键盘快捷键**：A键（区域）、E键（导出）
6. **多设备兼容**：安卓平板、手机浏览器

### 📊 数据管理
- **数据存储**：浏览器localStorage
- **导出格式**：CSV（Excel可打开）
- **数据隔离**：每个平板独立存储
- **备份恢复**：支持导入/导出

## 🎨 页面功能

### 签到流程
1. 平板打开对应区域链接
2. 显示"等待手环..."
3. 小朋友碰手环 → 显示姓名
4. 点击"✅ 到了！点这里签到"
5. 显示成功动画

### 教师功能
- **切换区域**：按键盘A键
- **导出记录**：按键盘E键
- **查看统计**：点击"查看记录"
- **清空数据**：管理界面操作

## 📈 迁移时间预估

| 任务 | 时间 | 备注 |
|:---|:---|:---|
| 创建GitHub仓库 | 5分钟 | 一次性 |
| 上传文件 | 10分钟 | 一次性 |
| 启用Pages | 2分钟 | 一次性 |
| 测试验证 | 15分钟 | 一次性 |
| 手环重新写入 | 8.5小时 | 101个手环×5分钟 |
| 教师培训 | 1小时 | 一次性 |

## 🔄 并行运行建议

### 第一阶段：测试验证（1-2天）
1. 部署到GitHub Pages
2. 更新5个手环测试
3. 新旧系统并行运行

### 第二阶段：逐步迁移（1周）
1. 按班级分批更新手环
2. 中一班 → 大一班 → 小一班 → 小二班
3. 每天更新1个班级

### 第三阶段：全面切换（1天后）
1. 确认所有手环已更新
2. 关闭旧系统提醒
3. 更新所有文档

## 📝 手环更新操作

### 使用NFC Tools APP
1. 打开NFC Tools APP
2. 选择"写"
3. 选择"URL/URI"
4. 输入：`https://[用户名].github.io/kindergarten-nfc/nfc-checkin.html#姓名`
5. 将手环靠近手机NFC区域
6. 听到提示音即成功

### 批量更新建议
- **按班级分组**：一次更新一个班级
- **标签管理**：已更新的手环贴标签
- **进度跟踪**：使用Excel表格记录

## 🚨 注意事项

### 数据安全
- ✅ 签到记录存储在设备本地
- ✅ 迁移不影响已有数据
- ✅ 可导出备份

### 兼容性
- ✅ 支持安卓平板（Chrome浏览器）
- ⚠️ iOS设备NFC功能有限
- ✅ 所有现代浏览器

### 网络要求
- ✅ 需要互联网访问GitHub Pages
- ✅ 校园网络通常可访问
- ✅ 支持离线缓存

## 📞 技术支持

### 常见问题
1. **页面打不开**：检查网络，尝试备用链接
2. **NFC不识别**：检查手环写入格式
3. **数据丢失**：导出备份后清空缓存

### 备用方案
- **备用链接**：保留freekit.dev链接作为备份
- **本地部署**：可部署到幼儿园内部服务器
- **多平台**：GitHub Pages + freekit.dev双保险

## 🎉 迁移完成检查清单

- [ ] GitHub仓库创建成功
- [ ] 文件上传完成
- [ ] GitHub Pages已启用
- [ ] 主页面可正常访问
- [ ] 区域链接测试通过
- [ ] 手环测试通过
- [ ] Excel表格已更新
- [ ] 使用指南已更新
- [ ] 教师培训完成
- [ ] 备份方案准备

---

**迁移完成时间**：2026-04-13  
**技术支持**：如有问题，请参考详细操作指南或联系技术支持