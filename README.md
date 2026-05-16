# EC-CUBE Snippets

EC-CUBE 4系の開発を効率化するVSCode拡張機能です。  
`ec` と打ち始めるだけで、Twig・PHP・YAMLのスニペットが補完候補に表示されます。  
各スニペットには日本語・英語の説明がツールチップで表示されます。

[![Visual Studio Marketplace](https://img.shields.io/visual-studio-marketplace/v/colscenery.eccube-snippets?label=VS%20Marketplace)](https://marketplace.visualstudio.com/items?itemName=colscenery.eccube-snippets)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE.txt)

---

## インストール

**拡張機能マーケットプレイス（Visual Studio Marketplace）からインストールできます。**  
👉 [EC-CUBE Snippets - Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=colscenery.eccube-snippets)

または、VS Code 内で以下の手順でインストールできます。

1. VS Code を開き、`Ctrl+P`（macOS: `Cmd+P`）でクイックオープンを起動
2. 以下のコマンドを貼り付けて Enter を押す

```
ext install colscenery.eccube-snippets
```

---

## 対応ファイル

- `.twig`
- `.html`
- `.php`
- `.yaml`
- `.yml`

---

## 使い方

1. `.twig` / `.html` / `.php` / `.yaml` / `.yml` ファイルを開く
2. `ec` と入力する
3. `eccube_` から始まる補完候補が一覧表示される
4. 選択するとスニペットが展開され、`Tab` キーで次の入力箇所に移動できる

**PHPスニペットについて**  
PHPスニペットには `<?php` が含まれていません。`<?php` タグの内側で使用してください。

---

## Twigスニペット一覧

### アセット（Asset）

| プレフィックス | 説明 |
|---|---|
| `eccube_asset_image` | 画像アセットのURL生成（user_data配下） |
| `eccube_asset_css` | CSSファイルの読み込みタグ生成 |
| `eccube_asset_js` | JavaScriptファイルの読み込みタグ生成 |
| `eccube_asset_plugin` | プラグイン内アセットのURL生成 |
| `eccube_asset_user_data_img` | user_data配下の画像をimgタグで表示 |
| `eccube_asset_user_data_download` | ダウンロード用アセットURL生成 |
| `eccube_asset_save_image_conditional` | save_image配下の画像を条件付き表示 |
| `eccube_asset_no_image_product` | no_image_productフィルターで商品画像を表示 |
| `eccube_product_image` | NO IMAGEフォールバック付き商品画像 |

### テンプレート構造（Template）

| プレフィックス | 説明 |
|---|---|
| `eccube_extends_default` | default_frame.twigを継承した基本ページ |
| `eccube_block_main` | mainブロックの定義 |
| `eccube_block_stylesheet` | CSS追加用stylesheetブロック |
| `eccube_block_javascript` | JS追加用javascriptブロック |
| `eccube_include` | 変数付きテンプレートinclude |
| `eccube_include_ignore` | エラーを無視するinclude |
| `eccube_set` | Twig変数の定義 |

### 条件・ループ（Control Flow）

| プレフィックス | 説明 |
|---|---|
| `eccube_if` | if条件分岐 |
| `eccube_if_else` | else付きif条件分岐 |
| `eccube_for_simple` | 汎用forループ（elseブロック付き） |
| `eccube_for_products` | 商品一覧ループ（画像・名前・価格・リンク付き） |
| `eccube_for_categories` | カテゴリ一覧リンクループ |
| `eccube_for_cart` | カートアイテムのループ処理 |

### フォーム（Form）

| プレフィックス | 説明 |
|---|---|
| `eccube_form_row` | `form_row()` によるフィールド一括レンダリング |
| `eccube_form_full` | フォーム全体（start〜end・CSRFトークン付き） |
| `eccube_form_manual` | label・widget・errorを個別レンダリング |
| `eccube_form_errors` | フォームエラーのみ表示 |
| `eccube_form_rest` | 未描画フォーム要素の出力 |

### カート（Cart）

| プレフィックス | 説明 |
|---|---|
| `eccube_cart_button` | カート追加フォームの基本マークアップ |
| `eccube_cart_link` | カートページへのリンク |

### パンくずリスト（Breadcrumb）

| プレフィックス | 説明 |
|---|---|
| `eccube_breadcrumb` | ループによるパンくずリスト |
| `eccube_breadcrumb_static` | 固定テキストのシンプルなパンくずリスト |

### URL・ルーティング（URL / Routing）

| プレフィックス | 説明 |
|---|---|
| `eccube_url` | ルート名から絶対URL生成 |
| `eccube_url_param` | パラメータ付きURL生成 |
| `eccube_path` | ルート名から相対パス生成 |
| `eccube_url_product_detail` | 商品詳細ページURL生成 |
| `eccube_url_product_list` | 商品一覧ページURL生成 |
| `eccube_url_product_list_category_color` | カテゴリ・color[]パラメータ付き商品一覧URL |
| `eccube_url_user_data_route` | eccube_user_data_routeによるURL生成 |
| `eccube_link_user_data_route` | 自由入力ページへのリンク |

### 認証・セキュリティ（Auth / Security）

| プレフィックス | 説明 |
|---|---|
| `eccube_csrf` | CSRFトークンhidden input |
| `eccube_login_check` | ログイン状態チェック |
| `eccube_is_granted` | 権限チェック |

### 価格・日付・翻訳（Filters）

| プレフィックス | 説明 |
|---|---|
| `eccube_price` | 価格の通貨フォーマット表示 |
| `eccube_price_inc_tax` | 税込価格の通貨フォーマット表示 |
| `eccube_date` | 日付のフォーマット表示 |
| `eccube_datetime` | 日時のフォーマット表示 |
| `eccube_trans` | 翻訳キーの表示 |
| `eccube_trans_param` | パラメータ付き翻訳の表示 |

### フラッシュ・ページネーション（UI）

| プレフィックス | 説明 |
|---|---|
| `eccube_flash` | フラッシュメッセージ一括表示 |
| `eccube_flash_type` | 種類指定フラッシュメッセージ表示 |
| `eccube_pagination` | ページネーション表示 |

### リクエスト・デバッグ・その他（Misc）

| プレフィックス | 説明 |
|---|---|
| `eccube_request_scheme_host` | スキーム付きホスト表示 |
| `eccube_request_pathinfo` | リクエストのパス情報表示 |
| `eccube_request_current_url` | 現在ページのURL生成 |
| `eccube_request_http_host` | サーバーパラメータからHTTP_HOST取得 |
| `eccube_request_host` | ホスト名表示 |
| `eccube_hook` | フックポイントのレンダリング |
| `eccube_admin_url` | 管理画面URLの生成 |
| `eccube_dump` | Twigデバッグ用dump |
| `eccube_comment` | Twigコメントの挿入 |

---

## PHPスニペット一覧

### クラス雛形（Class Scaffolding）

| プレフィックス | 説明 |
|---|---|
| `eccube_entity` | Entityクラスの雛形（Doctrine ORM付き） |
| `eccube_repository` | Repositoryクラスの雛形 |
| `eccube_form_type` | FormTypeクラスの雛形 |
| `eccube_controller` | プラグイン用Controllerクラスの雛形 |
| `eccube_admin_controller` | 管理画面用Controllerクラスの雛形 |
| `eccube_plugin_class` | PluginManagerクラスの雛形 |
| `eccube_event_subscriber` | テンプレートイベントSubscriberの雛形 |

### Entityプロパティ（Entity Properties）

| プレフィックス | 説明 |
|---|---|
| `eccube_getter_setter` | getterとsetterのセット生成 |
| `eccube_orm_column` | ORMカラムアノテーション付きプロパティ |
| `eccube_orm_many_to_one` | ManyToOneリレーションプロパティ |
| `eccube_orm_one_to_many` | OneToManyリレーションプロパティ |

### QueryBuilder

| プレフィックス | 説明 |
|---|---|
| `eccube_qb_find` | QueryBuilderによる複数件取得 |
| `eccube_qb_single` | QueryBuilderによる1件取得（nullセーフ） |

### Controllerユーティリティ（Controller Utilities）

| プレフィックス | 説明 |
|---|---|
| `eccube_add_success` | 成功フラッシュメッセージのセット |
| `eccube_add_error` | エラーフラッシュメッセージのセット |
| `eccube_redirect` | 指定ルートへのリダイレクト |
| `eccube_create_form` | フォーム生成・バリデーション・保存の一連処理 |

---

## YAMLスニペット一覧

### 設定ファイル（Config）

| プレフィックス | 説明 |
|---|---|
| `eccube_config_yaml` | プラグインのconfig.yaml生成 |
| `eccube_services_yaml` | services.yamlのプラグイン自動登録エントリ |

---

## 動作要件

- Visual Studio Code `1.75.0` 以上
- EC-CUBE 4系

---

## ライセンス

MIT

---

## リポジトリ・不具合報告

https://github.com/TakashiHishiki/eccube-snippets
