# sagaikun
 
[サイガイクン](https://code4fukui.github.io/saigaikun/)

![image](https://user-images.githubusercontent.com/1715217/156316472-5b6ed81d-18c4-4674-ac59-0e48cc2624ac.png)

## つくりかた

1. ブラウザで [ES-Jam](https://code4fukui.github.io/htmlprac/) を開く
2. 下記コードをコピペして、「見てみる」を押す
```html
<script type="module">
import { bg, show } from "https://js.sabae.cc/egadv.js";

await bg();
await show("強い地震が来ます！");
</script>
```
3. メッセージを追加する
```js
await show("強い地震が来ます！");
await show("より正しい選択をして、生き延びてください");
```
4. 選択肢のつくりかた
```js
const ans = await show("どうする？", ["たたかう", "にげる", "アイテム"]);
if (ans == "たたかう") {
    await show（”たたかった");
} else if (ans == "にげる") {
    await show（”にげた");
} else if (ans == "アイテム") {
    await show（”アイテムを使った");
}
```
5. ループのつくりかた （for と break）
```js
for (;;) {
    const ans = await show("どうする？", ["つづける", "おわる"]);
    if (ans == "おわる") {
        break;
    }
}
await show("ループおわり");
```
6. ページリンクのつくりかた
```js
document.location = "./";
```

## 作成レポート

### 良かったこと

- 大事なこと、知っておかないといけないと思いつつ、身近に感じないとやらないけど、ゲーム感覚だと抵抗がなくなる
  - ゲームで学ぶのはいいね
  - 県議GO、市議GOいいかも
- こんなに簡単にゲームがつくれたら、クラスの人とかと作って、
  - 二人でやってコうかするあだけで、楽しい

## 改善点

- 自分の持ち札があって、選べるようになるといい
  - 毎回同じ選択肢だとつまらない
  - 使う人によって選択肢が変わるようにしたい
- 背景を合わせて、地震とか火事とかでるといい
  - 車の背景に文字とかしたい
  - 絵が得意な人に作ってもらうのも良さそう

## ブログ

- [https://fukuno.jig.jp/3507](高専生が考える災害対策RPGスタイル「サイガイクン」とオープンソース体験ワークショップ)
- [https://fukuno.jig.jp/3533](高専先輩から学ぶ生きる戦略とシビックテック入門で充実「サイガイクン」)
 
