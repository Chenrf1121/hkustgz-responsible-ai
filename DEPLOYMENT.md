# HKUST-GZ Responsible AI Course Website

这是香港科技大学（广州）Responsible AI课程的官方网站。

## 部署到GitHub Pages

### 方法1：使用你自己的GitHub账号

1. **创建GitHub仓库**
   - 登录你的GitHub账号
   - 创建一个新的public仓库，名称为 `hkustgz-responsible-ai` 或任何你喜欢的名称

2. **初始化并推送代码**
   ```bash
   cd /home/RufengChen/hkustgz-responsible-ai

   # 如果需要，先删除原有的git历史
   rm -rf .git

   # 初始化新的git仓库
   git init
   git add .
   git commit -m "Initial commit: HKUST-GZ Responsible AI course website"

   # 添加你的GitHub仓库作为远程仓库（替换YOUR-USERNAME为你的GitHub用户名）
   git remote add origin https://github.com/YOUR-USERNAME/hkustgz-responsible-ai.git
   git branch -M main
   git push -u origin main
   ```

3. **配置GitHub Pages**
   - 进入仓库的Settings页面
   - 点击左侧的"Pages"
   - 在"Source"部分，选择"Deploy from a branch"
   - 选择"main"分支和"/ (root)"目录
   - 点击Save

4. **更新_config.yml**
   - 打开 `_config.yml` 文件
   - 修改以下两行：
     ```yaml
     baseurl: "/hkustgz-responsible-ai"  # 改为你的仓库名
     url: "https://YOUR-USERNAME.github.io/"  # 改为你的GitHub用户名
     ```
   - 提交并推送更改：
     ```bash
     git add _config.yml
     git commit -m "Update GitHub Pages configuration"
     git push
     ```

5. **访问网站**
   - 等待几分钟让GitHub Pages构建网站
   - 访问: `https://YOUR-USERNAME.github.io/hkustgz-responsible-ai/`

### 方法2：使用HKUST-GZ组织账号（推荐）

如果有HKUST-GZ的GitHub组织账号：

1. 在组织下创建仓库 `responsible-ai`
2. 按照上述步骤推送代码
3. 网站地址将会是: `https://hkust-gz.github.io/responsible-ai/`

### 方法3：自定义域名

如果你有自己的域名（如 `responsible-ai.hkust-gz.edu.cn`）：

1. 完成上述GitHub Pages部署
2. 在仓库根目录创建 `CNAME` 文件，内容为你的域名
3. 在域名DNS设置中添加CNAME记录指向 `YOUR-USERNAME.github.io`
4. 在GitHub仓库Settings > Pages中设置自定义域名

## 本地测试

在推送到GitHub之前，你可以在本地测试网站：

```bash
# 安装Jekyll（如果还没安装）
# Ubuntu/Debian:
sudo apt-get install ruby-full build-essential zlib1g-dev
gem install jekyll bundler

# 在项目目录下
cd /home/RufengChen/hkustgz-responsible-ai
bundle install

# 启动本地服务器
bundle exec jekyll serve

# 访问 http://localhost:4000/hkustgz-responsible-ai/
```

## 后续更新内容

完成部署后，你可以：

1. **更新教师信息**：编辑 `_data/people.yml`
2. **添加课程大纲**：在 `_lectures/` 目录添加更多讲座文件
3. **更新作业**：在 `_assignments/` 目录修改作业内容
4. **添加公告**：在 `_announcements/` 目录添加新公告
5. **上传课件**：将PDF、代码等文件放到 `static_files/` 目录

## 文件结构

```
.
├── _announcements/      # 公告
├── _assignments/        # 作业
├── _config.yml         # 网站配置（重要！）
├── _data/
│   └── people.yml      # 教师和TA信息
├── _events/            # 课程事件（考试、截止日期等）
├── _lectures/          # 讲座内容
├── _layouts/           # 页面布局模板
├── index.md            # 首页
├── materials.md        # 课程材料页面
├── project.md          # 项目页面
├── schedule.md         # 课程表页面
└── static_files/       # 静态文件（PDF、图片等）
```

## 需要帮助？

- Jekyll文档: https://jekyllrb.com/docs/
- GitHub Pages文档: https://docs.github.com/pages
- 模板原始仓库: https://github.com/kazemnejad/jekyll-course-website-template
