---
theme: seriph
background: https://source.unsplash.com/collection/94734566/1920x1080
class: text-center
highlighter: shiki
lineNumbers: false
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
drawings:
  persist: false
transition: slide-left
title: Welcome to Slidev
---

# ヘッドレスUIライブラリ

---

# 今日のひとこと

- リングフィットのおかげで体力がつく
- MacBookAir購入
- 望月峯太郎『座敷女』を読んだ

---

# Agenda

- ヘッドレスUIとは
- 関連ライブラリの説明
- まとめ

---

# ヘッドレスとは

- ディスプレイやキーボードなどの入出力機器を接続しない状態でコンピュータを運用すること
- 例) ヘッドレスCMS
  - 表示する画面がないCMSのこと

---

# ヘッドレスUIとは

- UIを「見た目」と「機能」にざっくり分ける
- 「機能」面のみを提供している
  - WAI-ARIA
  - 正しいセマンティクスと動作
  - キーボード操作
  - フォーカス
  - スクリーンリーダー対応

---

# Radix UI

https://www.radix-ui.com/

- 低レベルのUIコンポーネントライブラリ
  - アクセシビリティ
  - カスタマイズ性
  - 使いやすさ（開発者観点）
- デザインシステムのベースとしても使える
- React用

---

# Radix UI

- 時間削減が可能
  - 堅牢なUIコンポーネントの開発と保守には多くの時間がかかる
  - かつ未分化な作業（いくつかの要素が入り混じっていて複雑）
  - ビジネスロジックの開発に集中できる

---

# Radix UI

So, you think you can build a dropdown?

---

# Radix UI

- 完全なAPI設計
  - Unstyled
    - スタイルをオーバーライドする必要もなく、詳細度の争いも起こらない
  - Composable
    - 各構成部品へのきめ細やかなアクセス
  - Customizable
    - 動作の設定、フォーカスの制御、イベントリスナーの追加
  - Consistent
    - 似たような機能を持つコンポーネントは似た様なAPIを共有する

---

# Radix UI

- 追加が楽
  - 各コンポーネントは独立してバージョン管理されたパッケージになっている
    - Button だけインポート...とかが可能
    - 新しいコンポーネントを追加する際に干渉して書き換えが起こる心配はない
  - TypeScript フルサポート

---

# Radix UI

- Visually Hidden
  - アクセシビリティを担保した状態で表示を隠す

```tsx
import * as VisuallyHidden from '@radix-ui/react-visually-hidden';
import { GearIcon } from '@radix-ui/react-icons';

export default () => (
  <button>
    <GearIcon />
    <VisuallyHidden.Root>Settings</VisuallyHidden.Root>
  </button>
);
```

---

# Radix UI

- Accessible Icon
  - 既存のアイコンをラップすることで、見た目を変えずにラベルを付与できる

```tsx
import * as AccessibleIcon from '@radix-ui/react-accessible-icon';

export default () => (
  <AccessibleIcon.Root label="続きを読む">
      <some-icon/>
  </AccessibleIcon.Root>
);
```

---

# Base UI

https://mui.com/base-ui/getting-started/

- スタイルのない React UI コンポーネントと低レベルフックのライブラリ
  - すぐに使える機能を備えたコンポーネント
  - その機能を他のコンポーネントに転送するためのフック
- MUIからスタンドアロンパッケージとして利用できる
- 現在ベータ版

---

# Base UI

- 利点
  - MUI を利用する場合は Emotion を入れる必要がある
  - Base UI はスタイリングソリューションに依存しない

---

# Base UI

- 使い方の例
  - https://mui.com/base-ui/react-button/#hook

---

# headless UI

https://github.com/tailwindlabs/headlessui

- Tailwind CSS と統合するためにデザインされたヘッドレスUIコンポーネント
- React と Vue に対応
- https://headlessui.com/vue/menu#when-to-use-a-menu

---

# まとめ

- 色々あるね