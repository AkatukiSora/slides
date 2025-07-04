---
marp: true
paginate: true
theme: uncover
footer: 'Created by AkatukiSora'
---

<!-- _class: lead -->

# サーバーと1年間添い寝して  
### ― 案外悪くない生活だった ―
<!-- _speaker_notes:
「サーバーと一年間添い寝して」というタイトルで LT させて頂きます。  
前回の反省を生かして濃く短い発表を心がけました。よろしくお願いします！
-->

---

# ⚠️ 免責事項

<!-- _spealer_notes:
免責事項です
 -->

---

## ⚠️ 免責事項

- **背伸び**  
- **くそでか主語**

<!-- _speaker_notes:
この LT には多大なる背伸びとクソでか主語が含まれます。あらかじめご了承ください。
-->

---

## 📜 概要 (3行まとめ)

- **導入のハードルと現実** - 騒音/費用/場所
- **サーバーとの暮らし** - 案外悪くない
- **さあ、はじめよう** - 何でもサーバー化

<!-- _speaker_notes:
だいたいこんな流れです。詳細は後で爆速解説！
-->

---

# 👤 自己紹介

<!-- _speaker_notes:
自己紹介は
-->

---

# 👤🚫 省略

<!-- _speaker_notes:
省略します
-->

---

# ❤️ 欲しくなる理由（偏見）

- データの主権を渡したくない
<!-- -->
- マイクロ秒オーダーのNWレイテンシ
<!-- -->
- 仮想化されていない物理レイヤーに触れたい

<!-- _speaker_notes:
皆さんサーバーが欲しいと思うんですがその理由はこの辺になると思うんですよ。
手元で全部管理するのでデータの主権は自分ですし
物理的にもネットワーク的にも近いので極低レイテンシになります。
それに学習目的にも最高です。
-->

---

## 🛡️ 導入しない言い訳

- 騒音 (精神的コスト)
<!-- -->
- 費用 (金銭的コスト)
<!-- -->
- 場所 (空間的コスト)

<!-- _speaker_notes:
逆にしない言い訳としては大きく3つのコストがあると思います。
騒音と費用とあと場所です。
今回はこれらが実際に同棲してどうだったか簡単に話していこうと思います。
-->

---

## 🎧 騒音は慣れる

- 脳は適応型ノイズキャンセリング搭載
- 数時間で慣れて気にならなくなる

<!-- _speaker_notes:
まず騒音ですが。案外慣れます。
脳は長時間の連続する音を自動でフィルタする機能があります。  
ただ本当にうるさい場合は消音対策をとるか家庭内別居を！
でもそれ耳が悪くなってるのではと思うでしょう。
-->

---

## 👂 聴力は無事？

- 耳鼻科「異常なし、よく聞こえてるね」
- 枕元 **35 dB**

**騒音レベル比較:**
- WHO推奨 (日中): 40dB
- **自室の実測値: 35dB** (→ セーフ！！！！)

<!-- _speaker_notes:
実は聴力検査で「特に問題ないね」と言われました。朗報、サーバーと添い寝しても耳は無事です！
WHOの基準値も下回っており、一安心。
-->

---

## 💸 お金の問題

- ラックサーバー買っても中古 **3万円** 前後 
- 消費電力は意外に小さい (W程度)
- ラックサーバーじゃなくても OK

<!-- _speaker_notes:
現行機種を買わなければ案外安い。ヤフオクで 3 万円前後。  
電気代も 60 W 程度なら月 1,500 円くらいです。
-->

---

## 📍 場所がない問題

- 「**ラックは収納家具**」
- そうじゃなくても立てかけるなりできる
- そもそもミニPCとかであればもっとコンパクト

<!-- _speaker_notes:
ラックに棚板を付ければ立派な収納。  
場所を取るのではなく、それ自体が場所なのです。
それに立てかけるなりできますし、ラックだけが自宅サーバーの選択肢ではありません。
-->

---

## 🤖 何でもサーバーになる

- Linuxに洗脳できれば大体いける
- PC / ノパソ / 3DS / WiiU ...
- ~~(スペックはさておき)~~

<!-- _speaker_notes:
あとそもそも論としてLinuxが入ればだいたいサーバーにできます。
簡単なもので行けばデスクトップPCやミニPC、あとのノートパソコン、スマホ、3DS、WiiUなんかもいけると思います。
人によっては余ったパソコンが家にあったりすると思います。
それ、サーバーにできます。よかったですね、買うお金が浮きました。
-->

---

## 🛏️ ラックは安眠グッズ!?

- 悪夢→ラックを見る→安眠  
- n=1 ですが効果絶大  
- 心のセーフティネット

<!-- _speaker_notes:
悪夢で目覚めた深夜ってなんだか不安ですよね。
そんな時サーバー群を見て安心して二度寝した嘘みたいな話があります。  
ラックには安眠効果がある…気がします。異論があるかたはぜひ導入後にどうぞ！
-->

---

## 🚀 今夜、余り PC をサーバーに

- **行動喚起**  
- **そのPC、サーバーになります**
- #おうちDC布教

<!-- _speaker_notes:
ご清聴ありがとうございました。
今回のLTで、少しでも自宅サーバーへ興味を持ってくれると嬉しいです。
その余ったノートPCやスマホ、今夜からサーバー化してみませんか？
ハッシュタグ「#おうちDC布教」での投稿、お待ちしています！
-->

---

## 🗺️ うちの構成（ざっくり）

**構成:**
```
[Internet]
    | (Cloudflare Tunnel)
[Gateway/Router]
    |
[Proxmox VE]
  |-- [VMs] (サービス, メンテ用)
  |-- [Kubernetes] (サービス群)
```

<!-- _speaker_notes:
ネットワーク → Proxmox → VM/K8s の三層構成です。  
IP を外に晒したくないので Cloudflare Tunnel を併用しています。
-->

---

<!-- _class: lead -->

# まとめ & Next Step

- **サーバーはいいぞ。** 案外うるさくないし、高くない。
- **余ったPCはサーバーになる。** 今夜にでも始めよう。
- **最初の一歩:**
  - **余っているPC**を引っ張り出してくる(古くてOK)
  - **Ubuntu**をインストールしてみる
  - **nextcloud**とかインストールしよう

**さあ、あなたもサーバーのある生活へ！**

---

## ご清聴ありがとうございました

**AkatukiSora**

- **X (Twitter):** @AkatukiSora
- **GitHub:** AkatukiSora

---

## ❓ Q & A

- 「これサーバーになる？」大歓迎  
- 技術でも私生活でも OK

<!-- TODO: QRから直接発言しなくても質問できるサービスなんかを使うかも -->
<!-- _speaker_notes:
質問どうぞ！何でもサーバーになるか聞いてみてください。
-->

---

## ☣️ (尺稼ぎ) 物理事故集

- ラック収納で電源ボタン誤爆
<!-- -->
- Thin Provision → 物理枯渇で I/O 地獄
<!-- -->
- 家族がエアコン OFF

<!-- _speaker_notes:
時間が余れば語ります。足りなければここで終了！
-->

---

# ラック収納で電源ボタン誤爆

---

# Thin Provision ↓
# 物理領域枯渇で I/O 地獄

---

# 家族がエアコン OFF → 
# … ギリ無事
