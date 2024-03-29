## 简介

### 开发顺序

> 敏捷开发
> 
> 第一版实现: 文档上传和查看, OCR模型, NLP模型, 文档分类
>
> 之后考虑添加: 用户以及权限控制, 文档库

### 目标与背景

本项目的主要目标是设计一个智能文档自动识别与分类系统，利用OCR技术识别文档，结合NLP模型和推荐算法, 实现对文档的智能化处理。

```text
面对现代科技与信息化的不断提高，大学生在大学阶段产生的文档材料不断增多，例如成绩单、入党申请书、团员档案等。传统的手动整理文档工作效率低下，需要人员持续监督，增加了人力成本。因此，通过结合OCR技术和NLP深度学习算法，我们可以将这些文档自动化地分类、识别和管理，提高工作效率。
```

### 项目特色

- **智能分类：** 利用OCR技术将扫描版文档转换为文本，并通过推荐算法和NLP方法实现文档的自动分类。

- **推荐系统：** 基于用户上传文档的历史记录，引入推荐算法为文档自动分类提供参考，提高分类准确性。

- **用户友好界面：** 设计一个直观、易用的用户界面，使用户能够方便地上传和处理文档，并查看识别和分类的结果。

- **多层次管理**
  
  > 1. **文档库**层次 **(Not yet implemented)**:文档库是最高一个层次,用于组织和管理多个文档分类。每个文档库下可以包含多个文档分类。例如可以建立学生文档库、医院文档库，这样每个库可以分别设置权限。
  2. **文档分类**层次:文档分类属于特定的一个文档库,一个文档分类下可以包含多个文档。例如学生文档库下分类可能包括入党申请书、成绩单、学籍。
  3. **文档**层次:文档属于一个特定的文档分类,是最基础的管理单位。任何单个文档都属于此层次。

### 技术选择

- **前端:** React, Antd
- **后端:** FastAPI
- **关系数据库:** PostgreSQL
- **存储服务:** MinIO
- **OCR算法:** RapidOCR
- **NLP算法:** multilingual-e5-large-instruct
- **推荐算法:** pgvector


### 文件结构

- frontend
```text

```

- backend
```text

```