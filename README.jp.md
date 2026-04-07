# strawberry-autobuild-windows


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
| | ~~`x86` (32-bit)~~ | - | **提供終了**。QtおよびStrawberryによるサポートが終了。 |
| | `arm64` | Release, Debug | **試験的提供**（未検証） |
| **MinGW (MinGW-w64 GCC)** | `x64` (64-bit) | Release, Debug | GCCツールチェインを使用した代替ビルド |
| | `x86` (32-bit) | Release, Debug | **非推奨**。上流で削除済みのため、完動は保証されません。 |

- **Release:** パフォーマンスが最適化された、日常利用向けのビルドです。
- **Debug:** トラブルシューティング用のシンボルが含まれています。ファイルサイズが大きく、開発者向けです。

## 重要な注意点

- **アップデート機能を意図的に無効化しています：**
  本ビルドでは、内蔵の自動アップデート機能（Sparkle/QtSparkle）を**意図的に無効化**しています。これには以下の理由があります：
  1. **UX（ユーザー体験）の一貫性:** これらは非公式の自動ビルドであるため、公式のアップデート機能を有効にすると、更新のたびに公式リリース（主にPatreon等の寄付者向け案内）へのアップデートを促されることになります。このビルドをあえて選択しているユーザーにとって、こうした繰り返される通知は混乱を招き、利便性を損なうためです。
  2. **技術的な互換性:** これらのビルドは公式プロジェクトの証明書で署名されていません。そのため、公式の自動アップデート機能が正常に動作しない、あるいは互換性のないバイナリを案内してしまう可能性があります。
  3. **サポート負担の軽減:** アップデーターを無効化することで、ユーザーが（アクセス権のない、あるいは意図しない）公式版へ誤ってアップデートしてしまうのを防ぎます。また、非公式ビルドのユーザーから公式開発者へ、アップデートに関する不適切な問い合わせが行くことを避ける目的もあります。
  - *アップデートを行う際は、本リポジトリの「Releases」ページから最新版を手動でダウンロードしてください。*
- **x86 (32-bit) サポートの状況:**
  - **MSVC x86:** これらのビルドの提供を終了しました。QtフレームワークおよびStrawberry Music Playerプロジェクト本体において、32bit x86アーキテクチャのサポートが公式に終了したためです。
  - **MinGW x86:** 現在もビルド自体は生成されていますが、上流のリポジトリ（公式）からはx86向けの構成が既に削除されています。そのため、**すべての機能の動作や安定性は保証されません**。可能な限り、64bit版のWindowsへの移行を強く推奨します。
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