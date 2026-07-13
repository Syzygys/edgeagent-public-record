# EdgeAgent Public Record 项目状态

Last updated: 2026-07-13

## 目标

提供 Team C 的公开沉淀站，使每个发布数字能解析到本仓库文件与具体行号。本站只承载已经通过
`verify_publication.py` 的研究内容与必要证据，不承载私有 portfolio、token、交易凭证或未脱敏数据。

## 当前状态

- 公开仓库：`Syzygys/edgeagent-public-record`。
- Pages 来源：`main/docs`。
- 已发布内容：2026-07-11、2026-07-12、2026-07-13 的既有日报模板，本周频率 3 次。
- 初始机器审查：四个渠道 artifact 均为 `verified_ready`。
- 实际 Pages URL：`https://syzygys.github.io/edgeagent-public-record/`；Pages API 为 `built`，公开 URL HTTP 200。
- API 发现入口：GitHub homepage + 6 个 repository topics；计为 1 个真实流量池 listing。

## 发布规则

1. 既有模板必须先通过数字来源审查，再同步到本站。
2. 新栏目或新平台首发必须完成 24 小时否决窗。
3. 所有数字使用 `source: <repo>:<path>:<line>`，仓库别名由 `SOURCE_MAP.json` 解析。
4. 发布失败或协调仓库 push 失败必须把 Team C 状态写为 `DEGRADED`。
5. 每周至少重新审计已发布内容一次；数字漂移时下架并开 issue。

## 验证

- 本地站点生成：`python scripts/build_site.py`（在 Team C 工作区执行）。
- 数字审查：`python scripts/verify_publication.py`。
- 跨线复核：`python scripts/cross_line_diff.py`。
- 完成判据：远端仓库文件回读成功，Pages API 状态为 built，站点 URL 返回 HTTP 200。

## 已知问题

- X 发布身份尚未配置，本站上线不代表 X 已发布。
- 当前没有符合条件且具备可写 API 的 MCP/插件市场资产，流量池 listing 仍为 0。
- followers 当前未知；全组合仓库 stars 需每日通过 GitHub API 汇总。

## 下一步

- 将每日已审查模板同步到本仓库并保持每周至少三次发布。
- 配置 X 身份后启用 X 发布线。
- 出现可上架 MCP/plugin 资产时，优先选择有正式 API 且维护成本接近零的目录。
