## 前端页面设计

1. **首页**

  - 显示欢迎词

2. **文档分类管理页面（Category Management Page）**

  - 页面布局：采用卡片式布局，每个卡片展示一个文档分类。
  - 交互设计：用户点击分类卡片，页面跳转到对应的文档分类详情页面。
  - 在页面上提供"添加"操作按钮, 点击后弹出 _dialog_, 可以输入名称添加一个文档分类
  - 在每个分类卡片上提供"详情"、"编辑"、"删除"操作的按钮，允许用户进行相应的改名和删除操作。

    - 详情按钮: 跳转到对应的文档分类详情页面
    - 编辑按钮: 点击后弹出 _dialog_, 可以输入名称
    - 删除按钮: 点击后弹出 _popconfirm_, 其中包含确定和取消按钮, 如果再次点击确定按钮则执行删除

3. **文档分类详情页面（Category Details Page）**

  - 页面布局：以卡片形式展示该分类下的所有文档。
  - 在每个文档卡片上提供"查看 / 编辑"、"删除"操作的按钮，允许用户进行相应的改名和删除操作。

    - 查看 / 编辑按钮: 点击后弹出 _文档详情 modal_
    - 删除按钮: 点击后弹出 _popconfirm_, 其中包含确定和取消按钮, 如果再次点击确定按钮则执行删除

4. **上传文档页面（Upload Document Page）**

  - 页面布局：提供一个清晰的文件上传表单，用户可以上传文档。
  - 交互设计：上传后，系统自动进行OCR处理，并在页面上弹出 _dialog_ 展示处理结果和自动分类结果。

5. **搜索文档页面（Search Document Page）**

  - 页面布局：顶部提供一个搜索框，用户可以输入关键词进行搜索。
  - 交互设计：搜索结果以列表形式展示，每个结果旁边有"查看详情"按钮。点击后，弹出对应的 _文档详情 modal_。

6. **文档详情模态对话框（Document Details Modal）**

  - 对话框内容：展示文档的OCR识别结果、分类信息、图片存储URL等信息。
  - 操作选项：支持点击URL预览图片，以及关闭对话框的选项，提交 _modal_ 时根据其中的信息修改文档对应的信息。

    - 提交按钮: 根据 _modal_ 中的信息修改文档对应的信息
    - 取消按钮: 退出 _modal_

7. **导航栏（Navigation Bar）**

  - 设计：导航栏固定在页面的左侧，垂直布局。
  - 内容：包含以下按钮：

    - 首页：跳转到首页。 
    - 上传文档：跳转到上传文档页面。
    - 搜索文档：跳转到搜索文档页面。
    - 文档分类管理：跳转到文档分类管理页面。

  - 通过配置`frontend/.umirc.ts`中的`routes`参数来实现