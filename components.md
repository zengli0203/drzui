# Doro卡卡饮食健康小程序组件命名指南

## 项目概述

Doro卡卡是一款饮食健康追踪小程序，用户可以通过拍照上传每日饮食照片、跟踪卡路里摄入，并查看营养数据分析和趋势图表。项目采用了模块化设计，包含多个页面和可重用组件。

## 项目结构

### 页面 (Pages)

1. **首页 (index.html)**
   - 功能：作为应用主入口，集成了热量历史、当日饮食总览和餐食记录等核心模块
   - 入口：直接访问应用时的首页

2. **展示页 (pages/dashboard.html)**
   - 功能：展示今日热量和营养素比例，提供饮食评价和建议
   - 入口：导航栏第一项（图表图标）

3. **数据页 (pages/data.html)**
   - 功能：展示月历视图和历史趋势图表
   - 入口：导航栏第三项（图表趋势图标）

4. **个人主页 (pages/profile.html)**
   - 功能：用户信息展示、打卡签到、账号功能和自定义设置
   - 入口：导航栏第四项（个人图标）

5. **拍照页面 (pages/camera.html)**
   - 功能：提供拍照、上传照片和跳过拍照三种方式记录食物
   - 入口：各页面右下角悬浮拍照按钮

6. **餐食编辑页面 (pages/meal-edit.html)**
   - 功能：编辑餐食信息、查看营养分析和健康建议
   - 入口：
     - 拍照页面确认照片后
     - 点击首页餐食记录
     - 选择上传照片
     - 跳过拍照直接进入

### 组件 (Components)

#### 首页组件

1. **顶部标题栏 (Header)**
   - 类名：`.header`
   - 位置：首页顶部
   - 功能：显示应用名称"Doro卡卡"

2. **热量历史记录模块 (CalorieHistory)**
   - 类名：`.calorie-block`
   - 位置：标题栏下方
   - 功能：以垂直柱状图形式展示近7天热量摄入记录
   - 子组件：
     - 热量柱 (`.calorie-bar`)
     - 热量值 (`.calorie-value`)
     - 日期圆圈 (`.day-circle`) 
     - 日历按钮 (`.calendar-btn`)

3. **当日饮食总览模块 (DailyOverview)**
   - 类名：`.daily-overview`
   - 位置：热量历史记录下方
   - 功能：展示三大营养素比例和热量信息
   - 子组件：
     - 营养素进度条 (`.nutrient-progress`)
     - 热量卡片 (`.calorie-info`)

4. **当日餐食记录模块 (MealRecords)**
   - 类名：`.meal-records`
   - 位置：饮食总览下方
   - 功能：展示当日记录的各餐食物
   - 子组件：
     - 餐食卡片 (`.meal-card`)
     - 餐食时间标签 (`.meal-time-tag`)
     - 餐食图片 (`.meal-image`)

5. **拍照按钮 (CameraButton)**
   - 类名：`.floating-button`
   - 位置：右下角悬浮
   - 功能：快速进入拍照页面

6. **导航栏 (Navbar)**
   - 类名：`.nav-container`
   - 位置：页面底部
   - 功能：在不同页面间导航
   - 子组件：导航项 (`.nav-item`)

#### 拍照页面组件

1. **状态栏 (StatusBar)**
   - 类名：`.status-bar`
   - 位置：页面顶部
   - 功能：显示时间和系统状态图标

2. **顶部导航栏 (HeaderBar)**
   - 类名：`.header-bar`
   - 位置：状态栏下方
   - 功能：提供返回按钮和更多选项

3. **扫描框 (ScanFrame)**
   - 类名：`.scan-frame`
   - 位置：页面中央
   - 功能：提供食物拍照取景框
   - 子组件：
     - 扫描框四角 (`.scan-corner`)
     - 扫描线 (`.scan-line`)

4. **扫描选项栏 (ScanOptions)**
   - 类名：`.scan-options`
   - 位置：扫描框下方
   - 功能：提供不同扫描模式选择
   - 子组件：选项图标 (`.option-icon`)

5. **编辑按钮 (EditButton)**
   - 类名：`.edit-button`
   - 位置：右下角
   - 功能：跳过拍照直接进入编辑页面

6. **相机控制区 (CameraControls)**
   - 类名：`.camera-controls`
   - 位置：页面底部
   - 子组件：
     - 闪光灯按钮 (`.flash-button`)
     - 拍照按钮 (`.camera-button`)
     - 闪光灯选项 (`.flash-options`)
     - 闪光灯提示 (`.flash-tooltip`)

7. **预览模式 (PreviewMode)**
   - 类名：`.preview-mode`
   - 位置：全屏覆盖
   - 功能：拍照后预览照片
   - 子组件：
     - 预览图像 (`.preview-image`)
     - 预览控制栏 (`.preview-controls`)

#### 餐食编辑页面组件

1. **食物图片区域 (FoodImageArea)**
   - 类名：`.food-image`
   - 位置：页面顶部
   - 功能：展示食物图片
   - 子组件：
     - 导航栏 (`.navbar`)
     - 食物标签 (`.food-tag`)

2. **营养信息区域 (NutritionInfo)**
   - 类名：`.nutrition-info`
   - 位置：图片下方
   - 功能：包含食物分析和营养数据
   - 子组件：
     - 食物类型标签 (`.food-type-tag`)
     - 食物名称 (`.food-name`)
     - 数量控制器 (`.quantity-control`)
     - 营养素卡片 (`.nutrient-item`)
     - 评分进度条 (`.score-bar`)
     - 健康详情 (`.health-details`)

3. **底部操作区 (BottomActions)**
   - 类名：`.bottom-actions`
   - 位置：页面底部固定
   - 功能：提供主要操作按钮
   - 子组件：底部按钮 (`.bottom-button`)

## 设计规范

### 颜色系统

- **主色调**：绿色系列 (#15803D, #22c55e, #4ade80)
- **强调色**：蓝色 (#3B82F6)
- **警示色**：红色 (#ff9e9e)
- **中性色**：灰色系列 (#f8f9fa, #e5e7eb, #6b7280)

### 字体系统

- **主字体**：'PingFang SC', 'Helvetica Neue', Arial, sans-serif
- **标题字号**：大标题 24px (text-2xl)，小标题 20px (text-xl)
- **正文字号**：16px (text-base)
- **小字号**：14px (text-sm), 12px (text-xs)

### 间距系统

- **外边距**：4px, 8px, 16px, 24px, 32px (m-1, m-2, m-4, m-6, m-8)
- **内边距**：4px, 8px, 16px, 24px, 32px (p-1, p-2, p-4, p-6, p-8)
- **间隙**：4px, 8px, 16px, 24px (gap-1, gap-2, gap-4, gap-6)

### 圆角规范

- **大圆角**：20px, 24px (rounded-3xl, rounded-4xl)
- **中圆角**：12px, 16px (rounded-xl, rounded-2xl)
- **小圆角**：6px, 8px (rounded, rounded-lg)
- **全圆角**：9999px (rounded-full)

### 阴影规范

- **轻微阴影**：box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1) (shadow-sm)
- **普通阴影**：box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1) (shadow)
- **明显阴影**：box-shadow: 0 10px 15px rgba(0, 0, 0, 0.1) (shadow-lg)

## 交互规范

1. **按钮状态**
   - 正常状态：原色显示
   - 悬停状态：轻微加深背景色
   - 点击状态：scale(0.95) 缩小效果

2. **表单控件**
   - 输入框获得焦点：边框变色并微微加粗
   - 下拉菜单：点击展开，再次点击或点击外部关闭

3. **动画效果**
   - 过渡时间：0.2s-0.3s
   - 动画曲线：ease 或 ease-in-out
   - 关键动画：扫描线移动、健康详情展开/收起

## 响应式设计

- 页面设计基于375px宽度的移动设备
- 元素尺寸使用相对单位(rem, em)和百分比
- 文字大小使用响应式类(text-sm, text-base等)
- 布局使用Flexbox和Grid保证弹性
