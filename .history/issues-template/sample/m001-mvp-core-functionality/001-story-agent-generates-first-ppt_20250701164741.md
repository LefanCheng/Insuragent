# Title
Generate a Personalized PPT from a Proposal PDF

# Story
As a Hong Kong AIA Insurance Agent,
I want to upload a client's "Global Power Multi-Currency Plan 3" proposal PDF and type in their basic needs,
So that I can automatically get a professional, editable, and persuasive sales PPTX file in under 5 minutes, saving me hours of manual work and improving my sales effectiveness.

# Basic Concept
- PDF Proposal: Standardized insurance proposal document containing client information and product details
- PPTX Output: Editable PowerPoint presentation with professional sales narrative
- RAG Architecture: AI system combining knowledge base retrieval with generative capabilities
- FAB-P Script: Feature -> Advantage -> Benefit -> Presentation sales logic framework
- Persona Matching: AI analysis to match client needs with predefined customer archetypes

# Scenario
Preconditions:
- User has registered and logged into the system
- User has a valid "Global Power Multi-Currency Plan 3" proposal PDF
- User understands basic client needs and requirements

Main Flow:
1. User creates a new case in the system
2. User uploads the proposal PDF file
3. User enters client needs description in the text input field
4. System processes PDF and extracts key data (100% accuracy required)
5. AI analyzes input and matches with appropriate persona (Urban Young Professional or New Parent Family)
6. System generates personalized PPTX with professional sales narrative
7. User downloads the completed PPTX file

Exception Handling:
- Case 1: Invalid PDF format uploaded
  - Handling: Show clear error message and allow re-upload
- Case 2: PDF parsing fails or data extraction incomplete
  - Handling: Provide detailed error log and manual data entry option
- Case 3: AI analysis cannot match client to existing personas
  - Handling: Use default "Urban Young Professional" persona with generic content

# Acceptance Criteria
Functional Requirements:
- [ ] 用户可以成功注册和登录系统
- [ ] 用户可以创建一个新的客户案例 (Case)
- [ ] 用户可以成功上传一份「盈御多元貨幣計劃3」的PDF文件
- [ ] 用户可以在一个文本框中输入客户的自然语言描述
- [ ] 系统后台能100%准确地解析PDF中的关键数据（投保人、保费、缴费期、各年度保证/非保证价值等）
- [ ] AI能根据用户输入和我们预设的两个画像（都市奋斗青年/新手父母家庭），匹配并生成对应的销售逻辑和文案
- [ ] 系统能生成一份包含封面、需求回顾、数据增长图、概念图、FAB介绍等核心页面的PPTX文件
- [ ] 生成的PPTX文件在视觉风格上，与insuragent_lora_showcase.html的设计稿保持一致（色彩、字体、布局）
- [ ] 用户可以成功下载生成的PPTX文件

Non-functional Requirements:
- [ ] PDF解析准确率达到100%
- [ ] PPTX生成时间控制在5分钟以内
- [ ] 系统支持并发用户访问
- [ ] 生成的PPTX文件大小控制在合理范围内（<10MB）

# Sub-Issues
- [ ] 002-feat-user-auth
- [ ] 003-feat-pdf-parser
- [ ] 004-feat-knowledge-base-setup
- [ ] 005-feat-core-ai-logic
- [ ] 006-feat-ppt-generator
- [ ] 007-feat-frontend-flow
- [ ] 008-test-e2e-flow

# Dependencies
Technical Dependencies:
- [ ] {DEP-001} PDF parsing library (PyMuPDF/PDFPlumber)
- [ ] {DEP-002} LLM API integration (OpenAI/Claude)
- [ ] {DEP-003} PPTX generation library (python-pptx)
- [ ] {DEP-004} Vector database for knowledge base
- [ ] {DEP-005} Frontend framework (React/Vue)

Business Dependencies:
- [ ] {BIZ-001} AIA product knowledge and FAB-P scripts
- [ ] {BIZ-002} Customer persona definitions and analysis frameworks

# Status History
- 2025-01-27: Created 