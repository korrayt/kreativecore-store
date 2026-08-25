# Kreative Core Company Workflows — Kurulum

Bu paketin içeriğini `kreativecore-website` repository'sinin **kök dizinine** kopyalayın.

Son durumda şu yollar oluşmalıdır:

```text
kreativecore-website/
├── AGENTS.md
├── docs/company/...
└── .github/
    ├── ISSUE_TEMPLATE/
    │   └── company-task.yml
    ├── scripts/
    │   └── qa_gate.py
    └── workflows/
        ├── company-os-dispatcher.yml
        ├── worker-router.yml
        ├── qa-gate.yml
        └── company-status-report.yml
```

## İlk çalıştırma

1. Dosyaları repository'ye commit edin.
2. GitHub'da repository'yi açın.
3. `Actions` sekmesine girin.
4. `Kreative Core Company OS Dispatcher` workflow'unu seçin.
5. `Run workflow` düğmesine basın.
6. Workflow bir `Company OS — Initial Operating Cycle` issue'su açacaktır.
7. Bu issue'yu GitHub Copilot Coding Agent, Codex veya kullandığınız coding agent'a atayın.

## Gerekli repository ayarı

`Settings → Actions → General → Workflow permissions` bölümünde:

- `Read and write permissions`
- `Allow GitHub Actions to create and approve pull requests` yalnızca gerçekten gerekiyorsa

seçeneklerini değerlendirin.

Bu paketteki workflow'lar issue, label ve yorum oluşturabilmek için `issues: write` izni kullanır. QA workflow'u kaynak kodu sadece okur.

## Güvenlik

- API key, banka bilgisi, IBAN, özel anahtar veya seed phrase repository'ye yazılmamalıdır.
- Gerçek ödeme bilgileri GitHub Secrets veya hosting environment variables içinde tutulmalıdır.
- Merge ve canlı yayın kararı insan onayında kalır.
