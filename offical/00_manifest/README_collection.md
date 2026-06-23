# PQC PDF Collection

生成日期：2026-06-22  
用途：作为 `pqc-quickstart-tutor` 的第一版 PDF 资料库，用于支撑后量子密码快速入门讲课 Agent / Skill。

## 收集原则

1. 优先收集官方标准、官方状态报告、算法提交规范、作者维护站点的 specification PDF。
2. 不使用来源不明的转载 PDF、不使用商业宣传材料作为核心事实源。
3. NIST 标准状态、算法参数、密钥/密文/签名大小等事实，应以官方 FIPS / NIST 报告 / specification 为准。
4. 国内/中文方向单独放入 `05_china_related/`，作为研究与潜力方案资料；除非文件本身明确说明，不把这些材料视为正式国家标准。
5. 部分论文或网页已找到但下载受限，统一记录在 `not_included_or_failed.md`，不要让 Agent 假装这些 PDF 已经在库内。

## 目录说明

```text
pqc_pdf_collection/
├── 00_manifest/                         # 清单、来源说明、失败记录
├── 01_nist_standards/                   # 已发布 NIST 标准与 KEM 推荐
├── 02_nist_reports_migration/           # NIST PQC 标准化状态报告、迁移草案/白皮书
├── 03_selected_future_standards/         # Falcon/FN-DSA、HQC 等已选择但标准仍在推进的资料
├── 04_nist_additional_signatures_round3/ # NIST 附加签名 Round 3 候选规范
├── 05_china_related/                    # 国内/中文/中国相关 PQC 资料
└── 06_general_surveys/                  # 通用综述、迁移指南、应用场景资料
```

## Agent 使用建议

### 高可信事实源

优先使用：

- `01_nist_standards/`
- `02_nist_reports_migration/`
- `03_selected_future_standards/`
- `04_nist_additional_signatures_round3/` 中的算法官方 specification

适合回答：

- 标准状态；
- 算法名称和用途；
- 参数集；
- KeyGen / Encaps / Decaps / Sign / Verify 的官方流程；
- key / ciphertext / signature size；
- NIST 附加签名轮次状态。

### 教学与背景资料

可使用：

- `05_china_related/`
- `06_general_surveys/`

适合回答：

- 国内候选方向；
- 迁移背景；
- 工程部署挑战；
- PQC 在 TLS、关键基础设施、通信网络中的使用场景。

## 重要限制

- Falcon / FN-DSA 的最终 FIPS 206 在本资料包生成时仍未作为最终标准收录，因此这里只放 Falcon specification 与 NIST FIPS 206 状态材料。
- HQC 已被 NIST 选择用于标准化，但最终 FIPS 标准尚未收录在本资料包中，因此这里只放 HQC specification 与 NIST 第四轮报告。
- NIST 附加签名 Round 3 候选可能继续更新；`04_nist_additional_signatures_round3/` 应定期刷新。
- 中文/国内资料中，Aigis、SCloud+、LAC 等方案应作为“有潜力/研究方向/竞赛相关资料”使用，不应直接说成“已成为正式标准”。
