---
layout: home
title: ソラ向けLunatisプロジェクト概要
permalink: /sora-info/
---

# Lunatisプロジェクト概要

## はじめに
このサイトは、ソラAIにLunatisプロジェクトの現状と詳細を共有するためのものです。

## 全体アーキテクチャ

### プレイヤーアイコン移動制御システム

このシステムは、プレイヤーアイコンのマップ上での移動を管理します。

* **【Aモジュール】**: マップ画面でのクリックを検知し、Bモジュールに移動指示を伝達します。
    * GitHub Raw URL: `https://github.com/Tomo-141/info-for-sora/blob/main/_posts/example-a-module.md` (ここは後で実際のパスに変更)
* **【Bモジュール】**: クリックされた座標までプレイヤーアイコンを移動させます。移動中はCモジュールを呼び出し、移動完了時はDモジュールを呼び出します。
    * GitHub Raw URL: `https://github.com/Tomo-141/info-for-sora/blob/main/_posts/example-b-module.md`
* **【Cモジュール】**: プレイヤーアイコン移動中に、不要なクリックやマウスホイール操作を無効化します。
    * GitHub Raw URL: `https://github.com/Tomo-141/info-for-sora/blob/main/_posts/example-c-module.md`
* **【Dモジュール】**: プレイヤーアイコンの移動が完了した後、カメラを移動先の座標にセンタリングします。
    * GitHub Raw URL: `https://github.com/Tomo-141/info-for-sora/blob/main/_posts/example-d-module.md`

### 処理フロー：プレイヤーアイコン移動

**クリック開始**
　　⇩
**【Aモジュール】**(マップクリック検知)
　　⇩ (Bモジュールをコール)
**【Bモジュール】**(アイコン移動制御、移動中Cモジュールコール)
　　⇩ (移動完了時Dモジュールコール)
**【Dモジュール】**(画面センタリング)
　　⇧ (Bモジュール移動完了後)
**【Cモジュール】**(移動中、操作無効化)

---

### 用語集
* **Lunatis**: このプロジェクト全体の名称。RPGゲーム。
* **プレイヤーアイコン**: マップ上でプレイヤーの位置を示すキャラクター画像。---
layout: default
title: ソラ向けLunatisプロジェクト概要
permalink: /sora-info/
---

# Lunatisプロジェクト概要

## はじめに
このサイトは、ソラAIにLunatisプロジェクトの現状と詳細を共有するためのものです。

## 全体アーキテクチャ

### プレイヤーアイコン移動制御システム

このシステムは、プレイヤーアイコンのマップ上での移動を管理します。

* **【Aモジュール】**: マップ画面でのクリックを検知し、Bモジュールに移動指示を伝達します。
    * GitHub Raw URL: `https://github.com/Tomo-141/info-for-sora/blob/main/_posts/example-a-module.md` (ここは後で実際のパスに変更)
* **【Bモジュール】**: クリックされた座標までプレイヤーアイコンを移動させます。移動中はCモジュールを呼び出し、移動完了時はDモジュールを呼び出します。
    * GitHub Raw URL: `https://github.com/Tomo-141/info-for-sora/blob/main/_posts/example-b-module.md`
* **【Cモジュール】**: プレイヤーアイコン移動中に、不要なクリックやマウスホイール操作を無効化します。
    * GitHub Raw URL: `https://github.com/Tomo-141/info-for-sora/blob/main/_posts/example-c-module.md`
* **【Dモジュール】**: プレイヤーアイコンの移動が完了した後、カメラを移動先の座標にセンタリングします。
    * GitHub Raw URL: `https://github.com/Tomo-141/info-for-sora/blob/main/_posts/example-d-module.md`

### 処理フロー：プレイヤーアイコン移動

**クリック開始**
　　⇩
**【Aモジュール】**(マップクリック検知)
　　⇩ (Bモジュールをコール)
**【Bモジュール】**(アイコン移動制御、移動中Cモジュールコール)
　　⇩ (移動完了時Dモジュールコール)
**【Dモジュール】**(画面センタリング)
　　⇧ (Bモジュール移動完了後)
**【Cモジュール】**(移動中、操作無効化)

---

### 用語集
* **Lunatis**: このプロジェクト全体の名称。RPGゲーム。
* **プレイヤーアイコン**: マップ上でプレイヤーの位置を示すキャラクター画像。