# 户外运动签到系统 - 使用说明

## 核心链接
- **通用签到页**: https://freekit.dev/s/ejyVDEKU
- **手环链接模板**: `https://freekit.dev/s/ejyVDEKU#姓名`
- **示例（冯珺羿）**: `https://freekit.dev/s/ejyVDEKU#冯珺羿`

## 6个区域 · 平板默认链接

- **灌篮小乐宝**: https://freekit.dev/s/ejyVDEKU?area=灌篮小乐宝
- **IT小乐宝**: https://freekit.dev/s/ejyVDEKU?area=IT小乐宝
- **智驾小乐宝**: https://freekit.dev/s/ejyVDEKU?area=智驾小乐宝
- **智酷小乐宝**: https://freekit.dev/s/ejyVDEKU?area=智酷小乐宝
- **绳趣小乐宝**: https://freekit.dev/s/ejyVDEKU?area=绳趣小乐宝
- **芯动小乐宝**: https://freekit.dev/s/ejyVDEKU?area=芯动小乐宝

## 操作流程
1. **写入手环**: 用NFC Tools APP，选择"URL"类型，写入`{url}#[姓名]`
2. **设置平板**: 在每个区域的平板浏览器中打开对应的区域链接（如上面的6个链接）
3. **自动识别**: 平板页面自动设置为该区域，显示"等待手环..."
4. **签到**: 小朋友碰手环 → 显示姓名 → 点击"到了！点这里签到"
5. **管理**: 按"A"键可切换平板区域，按"E"键可导出记录

## 数据管理
- 数据存储在平板浏览器的localStorage中
- 可导出CSV、查看统计、批量清空
- 平板之间的数据**不共享**，需要分别导出
