# Content Exclusion 推奨パターン集（GitHub Copilot向け）

- 文書番号：`[SEC-COPILOT-CE-001]`
- 版数：`v0.1`
- 最終更新日：`[YYYY-MM-DD]`
- 対象：`Copilot Business / Enterprise`

---

## 1. 目的
本書は、GitHub CopilotのContent Exclusion設定を安全かつ実務的に適用するための推奨パターンを定義する。

## 2. 適用方針（基本）
1. **まず除外すべきものを明確化**：秘密情報、個人情報、顧客機密を優先。
2. **最小限から開始**：過剰除外で生産性を下げない。
3. **リポジトリ単位で差分管理**：全社共通＋案件固有ルールを分離。
4. **定期見直し**：四半期ごと、または事故・監査指摘時に更新。

## 3. 推奨パターン（共通・必須）
以下は原則として全社共通で除外する。

```txt
# 機密情報ファイル
**/.env
**/.env.*
**/*.pem
**/*.key
**/*.p12
**/*.pfx
**/id_rsa
**/id_ed25519
**/known_hosts

# クラウド/認証情報
**/.aws/**
**/.azure/**
**/.kube/**
**/secrets*.json
**/*secret*.json
**/*credentials*.json

# CI/CD・配布系の機密
**/.npmrc
**/.pypirc
**/nuget.config
**/NuGet.Config
**/docker-compose.override*.yml

# 証跡・ダンプ
**/*dump*.sql
**/*.bak
**/*.backup
**/*_backup_*
**/*_export_*

# 鍵/証明書の格納ディレクトリ
**/cert/**
**/certs/**
**/keys/**
```

## 4. 推奨パターン（条件付き）
以下はプロジェクト特性に応じて追加する。

```txt
# 契約・法務資料
**/contract/**
**/legal/**
**/*契約*.*
**/*NDA*.*

# 要件・設計の機微情報
**/requirements/**
**/architecture/**
**/*要件定義*.*
**/*基本設計*.*

# 顧客データ・移行データ
**/customer-data/**
**/migration-data/**
**/*顧客*.*
**/*個人情報*.*

# 監査/脆弱性報告
**/audit/**
**/pentest/**
**/*脆弱性*.*
**/*security-report*.*
```

## 5. C# / .NET プロジェクト向け追加推奨

```txt
# アプリ設定（環境依存）
**/appsettings.Production.json
**/appsettings.Staging.json
**/appsettings.Local.json

# ユーザーシークレットやローカル設定
**/secrets.json
**/*local.settings.json

# 配布前構成・署名関連
**/*.snk
**/*SignKey*.*
```

## 6. データベース運用向け追加推奨

```txt
# DB接続情報・運用情報
**/*connection*.*
**/*conn*.*
**/*dbconfig*.*
**/*postgresql.conf
**/*pg_hba.conf

# 運用ログ・実データ抽出
**/logs/**
**/*.log
**/*pgdiag*.*
**/*process_postgres*.csv
```

## 7. 除外ルール設計のアンチパターン
- `**/*.json` のような広すぎる除外（有用なコード文脈まで失う）
- 一時対応の除外を恒久化して放置
- 例外運用（緊急解除）時の証跡未記録
- ルール変更時に開発者へ周知しない

## 8. 運用手順（最小）
1. セキュリティ担当が初期パターン案を作成。
2. Tech Leadが開発影響をレビュー。
3. 管理者がOrg/Enterpriseへ反映。
4. 反映後、1週間は問い合わせ窓口を開設。
5. 月次で「追加/削除候補」を棚卸し。

## 9. 例外手続き（Content Exclusion個別）
- 申請対象：除外解除、限定解除、期間限定解除
- 必須情報：対象パス、理由、期間、代替策、承認者
- 承認要件：Tech Lead + セキュリティ担当の両承認
- 期限：最長`30日`、延長時は再申請

## 10. チェックリスト
- [ ] 秘密情報系パターンを適用済み
- [ ] 顧客機密系パターンを適用済み
- [ ] C#/.NET固有設定を確認済み
- [ ] DB運用ファイルの扱いを確認済み
- [ ] 例外申請フローを公開済み
- [ ] 見直し日（四半期）を設定済み

---

## 付録A：導入初期セット（コピペ用）

```txt
**/.env
**/.env.*
**/*.pem
**/*.key
**/*.p12
**/*.pfx
**/.aws/**
**/.azure/**
**/.kube/**
**/secrets*.json
**/*credentials*.json
**/appsettings.Production.json
**/appsettings.Staging.json
**/secrets.json
**/*postgresql.conf
**/*pg_hba.conf
**/logs/**
**/*.log
```

## 付録B：変更履歴
- `[YYYY-MM-DD]` v0.1 初版作成
