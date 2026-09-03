# PDF Renamer — update distribution

This repository contains update packages for installed copies of PDF Renamer.

**These files are not standalone application installers.**
They are consumed by an already-installed copy of PDF Renamer, which verifies
their signature before applying them. Downloading them directly will not give
you a working application.

## Contents

```
manifest.json                              latest version and where to find it
manifest.sig                               Ed25519 signature of manifest.json
releases/<version>/PDFRenamer_<version>.upd      update package
releases/<version>/PDFRenamer_<version>.upd.sig  Ed25519 signature of the package
```

## Verification

Every file is signed with an Ed25519 key held only by the maintainer.
The application verifies both `manifest.sig` and `<package>.upd.sig` against a
public key compiled into the application, and refuses to apply anything that
does not verify.

---

## 日本語

このリポジトリは、既にインストールされている PDF Renamer 向けの
**更新ファイル置き場**です。

**単体で動くインストーラではありません。** ここにあるファイルをダウンロードしても
アプリとしては使えません。インストール済みのアプリが署名を検証したうえで
適用するためのものです。

初回のインストール用の配布物はここには置いていません。配布元から受け取ってください。

すべてのファイルは開発者だけが持つ鍵で署名されており、
アプリは署名を検証できないものを一切適用しません。
