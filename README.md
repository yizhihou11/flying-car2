# 课程作业-2：亿航 EH216-S 无人驾驶载人 eVTOL 全方位安全分析

## 一、作业对照

| 作业要求 | 本产物对应情况 |
| --- | --- |
| 针对飞行汽车某技术/产品做深度安全分析 | 以亿航智能 EH216-S 无人驾驶载人 eVTOL 整机系统为对象 |
| 结合系统安全工程各方面 | 覆盖 FHA、FMEA、FTA、STPA、风险矩阵、冗余设计、残余风险与持续安全闭环 |
| 作业形式：Web 网页 | 单文件 `index.html`，内联 CSS/JS，无外部图片依赖，浏览器直接打开即可 |
| 入口文件：根目录 `index.html` | 仓库根目录即为 `index.html` |
| 仓库可见性：Public | 需在本人 GitHub 上设为 Public（见下方步骤） |
| 网页链接放入作业收集表 | 部署后把 Pages 链接粘贴到飞书收集表 |
| 截止时间 | 2026 年 11 月 26 日 18:00 前提交 |

## 二、网页内容结构

1. 产品与任务概述（构型、参数、任务剖面、系统边界）
2. 适航审定与标准框架（TC / AC / PC / OC 时间线、方法学）
3. 系统安全工程分析流程（FHA / FMEA / FTA / STPA）
4. 分域危险源识别（推进、能源、飞控航电、链路、环境、起降与乘员）
5. 风险评估与分级（5×5 风险矩阵 + 典型危险源定级表）
6. 安全设计与冗余防护体系
7. 典型失效场景推演（故障树 + STPA 不安全控制动作 + 处置链）
8. 残余风险与改进建议、持续安全闭环
9. 参考资料（含 CAAC 专用条件、指南及公开报道链接）

## 三、上传到 GitHub 并开启 Pages（交作业步骤）

### 方式 A：网页端上传（最简单）

1. 用本人账号在 GitHub 新建仓库：
   - 仓库名例如 `eh216s-safety-analysis`
   - **Visibility 选择 Public**
   - 不要勾选 “Add a README file”（本目录已自带 README）。
2. 进入仓库 → `Add file` → `Upload files`，把本文件夹里的 `index.html` 拖入；
   确保 `index.html` 在仓库**根目录**（不要放进子文件夹）。
3. 提交 Commit（Commit changes）。
4. 开启 Pages：仓库 `Settings` → 左侧 `Pages` →
   - `Branch` 选 `main`，文件夹选 `/ (root)`，保存。
5. 等待 1～2 分钟，访问 `https://<你的用户名>.github.io/<仓库名>/` 即可打开网页。
6. 把该链接填入作业收集表（飞书 wiki 收集链接）。

### 方式 B：Git 命令行

```bash
# 在本文件夹内
git init
git add index.html README.md
git commit -m "作业-2: EH216-S 全方位安全分析网页"

# 在 GitHub 新建 Public 仓库后，替换下面的用户名与仓库名
git remote add origin https://github.com/<你的用户名>/<仓库名>.git
git branch -M main
git push -u origin main
```

然后按方式 A 的第 4～6 步开启 Pages 并提交链接。

## 四、备注

- `index.html` 为单文件自包含页面，离线双击也能打开；字体走在线镜像，加载失败时自动回退系统字体。
- 报告中的风险等级为课程层面的定性工程判断；正式安全指标以 CAAC 适航审定文件与制造商技术手册为准。
- 如需要更换分析对象（如小鹏汇天、Joby、某子系统）或增删章节，直接修改 `index.html` 对应区块后重新提交即可。
