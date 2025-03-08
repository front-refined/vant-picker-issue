# vant date-picker 问题

## 背景

当 date-picker 存在 min-date 的配置时，且在滚动时还未等待滚动停止就点击了 confirm 按钮，输出的 selectedValues 错误（偶发性）

[components/date-picker](./src/components/date-picker/DatePicker.tsx) 和 [components/picker](./src/components/picker/Picker.tsx) 复制了 vant 的源码，
[components/picker](./src/components/picker/Picker.tsx) 做了[一行修改](./src/components/picker/Picker.tsx#L190)

## 测试视频

[测试视频](./public/1.mp4)

## 运行调试

```bash
pnpm install
pnpm run dev
```
