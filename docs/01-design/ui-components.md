# TaskAI UI组件库

## 📦 组件总览

TaskAI UI组件库包含所有可复用的界面元素，确保设计一致性和开发效率。

## 🎯 核心组件

### 1. 录音按钮组件 (VoiceRecordButton)

#### 大型录音按钮
```html
<div class="voice-record-btn-large">
  <div class="record-btn-inner">
    <i class="fas fa-microphone"></i>
  </div>
</div>
```

**样式规范：**
- **尺寸**：120px × 120px
- **背景**：白色渐变，阴影效果
- **图标**：48px，#667eea
- **状态**：正常、按下、录音中

**交互效果：**
- **悬停**：轻微放大(1.05倍)，阴影增强
- **按下**：缩放(0.95倍)，背景色变深
- **录音中**：脉冲动画，图标变红色

#### 录音中按钮
```html
<div class="voice-record-btn-recording">
  <div class="record-btn-inner pulse-animation">
    <i class="fas fa-stop"></i>
  </div>
</div>
```

### 2. 导航栏组件 (NavigationBar)

#### 顶部导航栏
```html
<header class="top-navigation">
  <div class="nav-left">
    <button class="back-btn">
      <i class="fas fa-arrow-left"></i>
    </button>
  </div>
  <div class="nav-center">
    <h1 class="page-title">页面标题</h1>
  </div>
  <div class="nav-right">
    <button class="action-btn">
      <i class="fas fa-ellipsis-v"></i>
    </button>
  </div>
</header>
```

**样式规范：**
- **高度**：64px
- **背景**：白色，底部边框
- **布局**：flex三栏布局
- **标题**：18px，粗体，居中

### 3. 任务卡片组件 (TaskCard)

#### 标准任务卡片
```html
<div class="task-card">
  <div class="task-status-indicator"></div>
  <div class="task-content">
    <div class="task-header">
      <h3 class="task-title">任务标题</h3>
      <div class="task-actions">
        <button class="task-action-btn">
          <i class="fas fa-edit"></i>
        </button>
        <button class="task-action-btn">
          <i class="fas fa-trash"></i>
        </button>
      </div>
    </div>
    <div class="task-meta">
      <span class="task-date">今天</span>
      <span class="task-tag">重要</span>
    </div>
  </div>
  <div class="task-checkbox">
    <input type="checkbox" id="task-1">
    <label for="task-1"></label>
  </div>
</div>
```

#### 分组任务卡片
```html
<div class="task-group-card">
  <div class="group-header">
    <div class="group-title">
      <i class="fas fa-chevron-down"></i>
      <span>主任务标题</span>
    </div>
    <div class="group-progress">
      <span>2/3 完成</span>
    </div>
  </div>
  <div class="subtasks">
    <div class="subtask-item">
      <input type="checkbox" id="subtask-1" checked>
      <label for="subtask-1">子任务1</label>
    </div>
    <div class="subtask-item">
      <input type="checkbox" id="subtask-2">
      <label for="subtask-2">子任务2</label>
    </div>
  </div>
</div>
```

### 4. 处理进度组件 (ProcessingProgress)

#### 步骤进度指示器
```html
<div class="processing-steps">
  <div class="step-item completed">
    <div class="step-icon">
      <i class="fas fa-volume-up"></i>
    </div>
    <div class="step-content">
      <div class="step-title">语音识别</div>
      <div class="step-status">✓ 完成</div>
      <div class="step-progress">
        <div class="progress-bar" style="width: 100%"></div>
      </div>
    </div>
  </div>

  <div class="step-item active">
    <div class="step-icon">
      <i class="fas fa-brain pulse-animation"></i>
    </div>
    <div class="step-content">
      <div class="step-title">AI分析</div>
      <div class="step-status">
        <i class="fas fa-sync-alt animate-spin"></i>
        进行中...
      </div>
      <div class="step-progress">
        <div class="progress-bar" style="width: 65%"></div>
      </div>
    </div>
  </div>
</div>
```

#### 圆形进度指示器
```html
<div class="circular-progress">
  <svg class="progress-ring" viewBox="0 0 100 100">
    <circle cx="50" cy="50" r="45" fill="none" stroke="#e5e7eb" stroke-width="8"></circle>
    <circle class="progress-ring-circle" cx="50" cy="50" r="45" fill="none"
            stroke="#3b82f6" stroke-width="8"
            stroke-dasharray="283" stroke-dashoffset="99"></circle>
  </svg>
  <div class="progress-text">
    <span class="progress-percentage">65%</span>
    <span class="progress-label">处理进度</span>
  </div>
</div>
```

### 5. 输入组件 (InputComponents)

#### 搜索输入框
```html
<div class="search-input-container">
  <i class="fas fa-search search-icon"></i>
  <input type="text" class="search-input" placeholder="搜索任务...">
  <button class="clear-search-btn">
    <i class="fas fa-times"></i>
  </button>
</div>
```

#### 标准输入框
```html
<div class="input-container">
  <label class="input-label">标签文字</label>
  <input type="text" class="text-input" placeholder="请输入...">
  <div class="input-error">错误信息</div>
</div>
```

### 6. 按钮组件 (Buttons)

#### 主要按钮
```html
<button class="btn btn-primary">
  <i class="fas fa-check"></i>
  确认保存
</button>
```

#### 次要按钮
```html
<button class="btn btn-secondary">
  <i class="fas fa-plus"></i>
  添加任务
</button>
```

#### 危险按钮
```html
<button class="btn btn-danger">
  <i class="fas fa-trash"></i>
  删除
</button>
```

#### 图标按钮
```html
<button class="btn-icon">
  <i class="fas fa-edit"></i>
</button>
```

### 7. 设置项组件 (SettingItem)

#### 标准设置项
```html
<div class="setting-item">
  <div class="setting-left">
    <div class="setting-icon">
      <i class="fas fa-bell"></i>
    </div>
    <div class="setting-content">
      <div class="setting-title">任务提醒</div>
      <div class="setting-desc">接收任务到期提醒</div>
    </div>
  </div>
  <div class="setting-right">
    <div class="toggle-switch">
      <input type="checkbox" id="setting-1" checked>
      <label for="setting-1"></label>
    </div>
  </div>
</div>
```

#### 链接设置项
```html
<div class="setting-item clickable">
  <div class="setting-left">
    <div class="setting-icon">
      <i class="fas fa-user"></i>
    </div>
    <div class="setting-content">
      <div class="setting-title">账户信息</div>
      <div class="setting-desc">管理个人信息</div>
    </div>
  </div>
  <div class="setting-right">
    <i class="fas fa-chevron-right"></i>
  </div>
</div>
```

### 8. 状态指示器组件 (StatusIndicator)

#### 状态徽章
```html
<span class="status-badge success">已完成</span>
<span class="status-badge processing">进行中</span>
<span class="status-badge pending">待处理</span>
```

#### 进度条
```html
<div class="progress-container">
  <div class="progress-bar-container">
    <div class="progress-bar-fill" style="width: 75%"></div>
  </div>
  <span class="progress-text">75%</span>
</div>
```

### 9. 列表组件 (ListComponents)

#### 筛选标签列表
```html
<div class="filter-tabs">
  <button class="filter-tab active">全部</button>
  <button class="filter-tab">今天</button>
  <button class="filter-tab">重要</button>
  <button class="filter-tab">工作</button>
</div>
```

#### 空状态列表
```html
<div class="empty-state">
  <div class="empty-icon">
    <i class="fas fa-clipboard-list"></i>
  </div>
  <div class="empty-title">暂无任务</div>
  <div class="empty-desc">点击下方按钮创建第一个任务</div>
  <button class="btn btn-primary">
    <i class="fas fa-plus"></i>
    创建任务
  </button>
</div>
```

### 10. 模态框组件 (Modal)

#### 标准模态框
```html
<div class="modal-overlay">
  <div class="modal-container">
    <div class="modal-header">
      <h3 class="modal-title">标题</h3>
      <button class="modal-close">
        <i class="fas fa-times"></i>
      </button>
    </div>
    <div class="modal-body">
      <p>模态框内容</p>
    </div>
    <div class="modal-footer">
      <button class="btn btn-secondary">取消</button>
      <button class="btn btn-primary">确认</button>
    </div>
  </div>
</div>
```

## 🎨 组件样式定义

### 基础样式变量
```css
:root {
  /* 颜色变量 */
  --primary-color: #667eea;
  --secondary-color: #764ba2;
  --success-color: #10b981;
  --error-color: #ef4444;
  --warning-color: #f59e0b;
  --processing-color: #3b82f6;
  --waiting-color: #9ca3af;

  /* 字体变量 */
  --font-size-xs: 12px;
  --font-size-sm: 14px;
  --font-size-base: 16px;
  --font-size-lg: 18px;
  --font-size-xl: 22px;
  --font-size-2xl: 28px;

  /* 间距变量 */
  --spacing-xs: 4px;
  --spacing-sm: 8px;
  --spacing-md: 16px;
  --spacing-lg: 24px;
  --spacing-xl: 32px;

  /* 圆角变量 */
  --border-radius-sm: 4px;
  --border-radius-md: 8px;
  --border-radius-lg: 12px;
  --border-radius-full: 50%;

  /* 阴影变量 */
  --shadow-sm: 0 1px 3px rgba(0,0,0,0.1);
  --shadow-md: 0 4px 6px rgba(0,0,0,0.1);
  --shadow-lg: 0 10px 25px rgba(0,0,0,0.15);
  --shadow-button: 0 10px 25px -5px rgba(102, 126, 234, 0.4);
}
```

### 通用工具类
```css
.flex-center { display: flex; align-items: center; justify-content: center; }
.flex-between { display: flex; align-items: center; justify-content: space-between; }
.text-center { text-align: center; }
.text-left { text-align: left; }
.text-right { text-align: right; }

.w-full { width: 100%; }
.h-full { height: 100%; }

.cursor-pointer { cursor: pointer; }
.cursor-not-allowed { cursor: not-allowed; }

.transition { transition: all 0.3s ease; }
.transition-fast { transition: all 0.15s ease; }
```

## 🎯 组件使用指南

### 使用原则
1. **一致性**：在所有页面中使用相同的组件样式
2. **可访问性**：确保所有组件支持键盘导航和屏幕阅读器
3. **响应式**：组件应适配不同屏幕尺寸
4. **性能**：避免过度使用动画和复杂效果

### 自定义指南
1. **颜色**：使用CSS变量定义的颜色
2. **间距**：遵循8px网格系统
3. **字体**：使用指定的字体大小和字重
4. **动画**：使用统一的缓动函数和时长

### 组件组合
1. **布局**：使用flex和grid进行布局
2. **嵌套**：避免过深的组件嵌套
3. **复用**：优先使用现有组件，避免重复开发

---

**文档版本：** 1.0
**最后更新：** 2024年11月
**负责人：** 设计团队
**维护状态：** 持续更新

这份UI组件库为TaskAI项目提供了完整的组件设计规范，确保开发过程中的一致性和效率。