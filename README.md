# secret-triage-demo

验证「分诊 → SARIF → 代码扫描」整条链。真实的噪声（规则文件、测试夹具）不应出现在 Security 页；只有真密钥形态会。

## 验证结果（2026-11-24）

输入 3 条 → Code Scanning 里实际出现 **1 条**：

```
secret-triage/real-secret | src/leak.js:1
```

`rules/aws.yml` 与 `tests/redact.spec.ts` **没有进入 Security 页**。

该告警为合成样本，验证后已 dismiss（won't fix）。
