# strawberry-autobuild-windows

---

[![Build](https://github.com/stm7128/strawberry-autobuild-windows/actions/workflows/build.yml/badge.svg)](https://github.com/stm7128/strawberry-autobuild-windows/actions/workflows/build.yml)

[English](https://github.com/stm7128/strawberry-autobuild-windows/blob/main/README.md) | **日本語** 

このリポジトリは、[Strawberry Music Player](https://github.com/strawberrymusicplayer/strawberry) の非公式 **Windows ビルド**を提供します。

**ダウンロード:** 最新の非公式ビルドは [**Releases ページ**](https://github.com/stm7128/strawberry-autobuild-windows/releases/latest) からダウンロードできます。

現在、公式プロジェクトからはすべてのユーザー向けのWindowsビルドが直接提供されていません。ソースコードからビルドする手順については、[公式リポジトリの説明](https://github.com/strawberrymusicplayer/strawberry#wrench-compiling-from-source) をご覧ください。

## 利用可能なビルド

このリポジトリでは、以下の種類のWindowsビルドを提供しています。ビルドは、公式のStrawberryリポジトリの最新コードを元に、毎日（およびこのリポジトリの`main`ブランチへのプッシュ時）自動的に生成されます。

| ツールチェイン | アーキテクチャ | ビルドタイプ | 備考 |
| :--- | :--- | :--- | :--- |
| **MSVC (Microsoft Visual C++)** | `x86_64` (64-bit) | Release, Debug | **ほとんどのユーザーに推奨** |
| | `x86` (32-bit) | Release, Debug | |
| | ~~`arm64`~~ | ~~Release~~, ~~Debug~~ | **このビルドは不安定かつ検証不可能なため廃止しました。** |
| **MinGW (MinGW-w64 GCC)** | `x86_64` (64-bit) | Release, Debug | GCCを使用した代替ビルド |
| | `x86` (32-bit) | Release, Debug | |

- **Release:** 日常的な使用のために最適化されたビルドです。ほとんどのユーザーはこちらを選択してください。
- **Debug:** ファイルサイズが大きい、開発者や特定の問題を調査するためのビルドです。

## 重要な注意点

*   **アップデーターの無効化:** この非公式ビルドに搭載されている自動更新機能は、意図的に無効化されています。これは、本ビルドが独立して提供されているものであり、公式の更新メカニズムを使用すると、ユーザーが混乱したり、公式プロジェクトの支援者を対象としたPatreonページへ誤って誘導されたりする可能性があるためです。更新する際は、このリポジトリの [Releases ページ](https://github.com/stm7128/strawberry-autobuild-windows/releases/latest) から最新版をダウンロードしてください。

## 問題とサポート

*   **Strawberryの機能**に関するバグ、問題、機能リクエストは、公式の [Strawberry Issues ページ](https://github.com/strawberrymusicplayer/strawberry/issues) に報告してください。Strawberryの開発者がGitHub経由で対応してくれる可能性があります。
    *   *（例：音楽の再生が途切れる、特定のファイル形式が再生できない、新しいオーディオ出力に関する機能リクエストなど）*

*   **このリポジトリが提供するビルドプロセス、インストーラー、またはビルドの可用性**に特化した問題が発生した場合は、[こちらのIssues](https://github.com/stm7128/strawberry-autobuild-windows/issues) に報告してください。
    *   *（例：インストーラーが実行できない、ダウンロードしたファイルが破損している、定期ビルドが失敗しているなど）*

このリポジトリは、Strawberry Music Player自体の公式サポートを提供するものではありません。

## ライセンス

`Strawberry Music Player`はGPLv3ライセンスで提供されています。これらの非公式ビルドも、GPLv3の条項に基づいて提供されます。

## 公式開発のサポート

この度は、Strawberry Music Playerの非公式ビルドをご利用いただきありがとうございます。もしこのソフトウェアを気に入っていただけましたら、以下の方法で公式開発のサポートをご検討ください。**公式開発者を直接支援する**ことは、Strawberryの継続的な開発とメンテナンスに繋がります。

- [Patreon](https://www.patreon.com/jonaskvinge) - 支援者は公式ビルドを入手できる場合があります。現在の特典やプランについては、各ページをご確認ください。
- [GitHub Sponsors](https://github.com/sponsors/jonaski)
- [Ko-fi](https://ko-fi.com/jonaskvinge) - こちらも支援者向けに公式ビルドが提供される場合があります。詳細はページをご確認ください。
- [PayPal](https://paypal.me/jonaskvinge)