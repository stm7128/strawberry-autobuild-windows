# strawberry-autobuild-windows

---

[![Build](https://github.com/stm7128/strawberry-autobuild-windows/actions/workflows/build.yml/badge.svg)](https://github.com/stm7128/strawberry-autobuild-windows/actions/workflows/build.yml)

[English](https://github.com/stm7128/strawberry-autobuild-windows/blob/main/README.md) | **日本語** 

このリポジトリは、[Strawberry Music Player](https://github.com/strawberrymusicplayer/strawberry) の非公式 **Windows ビルド**を提供します。

**ダウンロード:** 最新の非公式ビルドは [**Releases ページ**](https://github.com/stm7128/strawberry-autobuild-windows/releases/latest) からダウンロードできます。

現在、公式プロジェクトからはすべてのユーザー向けのWindowsビルドが直接提供されていません。ソースコードからビルドする手順については、[公式リポジトリの説明](https://github.com/strawberrymusicplayer/strawberry#wrench-build-from-source) をご覧ください。

## 利用可能なビルド

ビルドは、公式のStrawberryリポジトリの最新コードを元に、毎日（およびこのリポジトリの`main`ブランチへのプッシュ時）自動的に生成されます。

| ツールチェイン | アーキテクチャ | ビルドタイプ | 備考 |
| :--- | :--- | :--- | :--- |
| **MSVC (Microsoft Visual C++)** | `x64` (64-bit) | Release, Debug | ほとんどのWindowsユーザーに**推奨** |
| | `x86` (32-bit) | Release, Debug | 32bit Windowsシステム用 |
| | `arm64` | Release, Debug | **試験的提供**（未検証） |
| **MinGW (MinGW-w64 GCC)** | `x64` (64-bit) | Release, Debug | GCCツールチェインを使用した代替ビルド |
| | `x86` (32-bit) | Release, Debug | |

- **Release:** パフォーマンスが最適化された、日常利用向けのビルドです。
- **Debug:** トラブルシューティング用のシンボルが含まれています。ファイルサイズが大きく、開発者向けです。

## 重要な注意点

- **アップデーターの無効化:** このビルドでは自動更新機能が意図的に無効化されています。これは、本ビルドが公式とは異なるチャンネルで提供されていることによる混乱を防ぎ、また公式プロジェクトの支援メカニズムを損なわないようにするためです。更新する際は、このリポジトリから手動で最新版をダウンロードしてください。
- **ARM64ビルドの試験的ステータス:** ARM64ビルドの提供を再開しましたが、これらは**試験的なもの**です。管理者はARM64 Windowsの実機（Snapdragon X Elite等）を所有していないため、**動作確認は一切行われていません**。ARM64デバイスをご利用の方で、動作の成否や不具合などの報告をいただける場合は、[GitHub Issues](https://github.com/stm7128/strawberry-autobuild-windows/issues) までフィードバックをいただけると助かります。

## 透明性

セキュリティと信頼性を確保するため、すべてのビルドは [GitHub Actions](https://github.com/stm7128/strawberry-autobuild-windows/actions) で自動化されています。
ビルドプロセスでは以下の変更を行っています：
- CMakeの設定で自動更新機能を無効化しています (`-DENABLE_QTSPARKLE=OFF`)。
- インストーラースクリプト (`.nsi`) に、上記設定に合わせるためのパッチを適用しています。
- Strawberryのソースコード本体には、これら以外の改変は一切加えていません。

## 問題とサポート

- **Strawberry 本体のバグ報告:** （例：再生の不具合、UIのバグ、機能リクエストなど）は、公式の [Strawberry Issues ページ](https://github.com/strawberrymusicplayer/strawberry/issues) に報告してください。
  - *注：公式に報告する際は、混乱を避けるため「**非公式ビルドを使用していること**」を明記してください。*
- **ビルドやインストーラーに関する問題:** （例：インストーラーが起動しない、DLLが足りない、リンク切れなど）は、[このリポジトリのIssues](https://github.com/stm7128/strawberry-autobuild-windows/issues) に報告してください。

## ライセンス

Strawberry Music PlayerはGPLv3ライセンスで提供されています。これらの非公式ビルドおよび本リポジトリのビルドスクリプトも、GPLv3の条項に基づいて提供されます。

## 公式開発のサポート

Strawberry Music Playerを気に入っていただけましたら、公式開発者である **Jonas Kvinge** 氏への支援をぜひご検討ください。公式開発者を直接支援することは、プロジェクトの継続と将来的な発展に繋がります。

- [Patreon](https://www.patreon.com/jonaskvinge) - 支援者は公式ビルドを入手できる場合があります。現在の特典やプランについては、各ページをご確認ください。
- [GitHub Sponsors](https://github.com/sponsors/jonaski)
- [Ko-fi](https://ko-fi.com/jonaskvinge) - こちらも支援者向けに公式ビルドが提供される場合があります。詳細はページをご確認ください。
- [PayPal](https://paypal.me/jonaskvinge)