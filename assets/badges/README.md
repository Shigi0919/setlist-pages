# ストアバッジ

App Store と Google Play の公式バッジ。**自作せず、配布された素材をそのまま置いている。**
両社とも「改変するな」と明記しているので、色・比率・要素の配置に手を加えないこと。

| ファイル | 配布元 | 取得日 |
|---|---|---|
| `app-store-ja.svg` | Apple: `https://toolbox.marketingtools.apple.com/api/v2/badges/download-on-the-app-store/black/ja-jp` | 2026-10-08 |
| `app-store-en.svg` | Apple: `https://toolbox.marketingtools.apple.com/api/v2/badges/download-on-the-app-store/black/en-us` | 2026-10-08 |
| `google-play-ja.svg` | Google Partner Marketing Hub「Google Play Badge guidelines」(2026-06-25版) | 2026-10-08 |
| `google-play-en.svg` | 同上 | 2026-10-08 |

Google の配布元: <https://partnermarketinghub.withgoogle.com/brands/google-play/google-play/lockups-icons-badges/>
（旧 `play.google.com/intl/*/badges/` はここへリダイレクトされる。旧URLで配信されている
PNG は 2022年以前の古い意匠なので使わないこと。Google は「古いバッジを使うな」と明記している。）

Apple のガイドライン: <https://developer.apple.com/app-store/marketing/guidelines/>

## 守っている決まり

**色。** App Store は黒を使う。Apple は「他プラットフォームのバッジが同じ中に出る場合は、
白ではなく黒を使う」と規定している。Google Play のバッジには配色違いが存在しない（1種類のみ。
濃色背景用の "Reverse" があるのはロゴロックアップで、バッジではない）。
そのため最終CTAのオレンジ背景でも、両方とも黒のまま並べている。

**サイズ。** 表示高さ 48px。最小は Apple が 40px、Google が 28px。
Google は「他ストアのバッジと同じか大きく」が要件なので、高さを揃えた上で幅は Google が広い
（162px に対し App Store は 131〜144px）。

**余白。** 両社とも最小クリアスペースは「バッジ高さの 1/4」＝ 12px。
`.store-btns` の `gap` は 16px、上下も 16px 以上空けている。

**動かさない。** ホバーで拡大・移動・色変更をしない。Apple は「バッジをアニメーションさせない」、
Google は「効果を加えない」と明記している。

**文字を添えない。** バッジ内に「App Store からダウンロード」等が入っているので、
横に自前のラベルを置かない（以前の自作ボタンはここが二重になっていた）。

**言語。** マーケティングの言語に合わせたローカライズ版を使う。
LP の `[data-lang]` による日英の出し分けに乗せている。

## 注意

日本語の Google Play バッジは、公式バンドルの `Digital/svg/` に Web版が入っていない。
入っているのは `GetItOnGooglePlay_Badge_Print_color_Japanese.svg` のみ。
一方 `Digital/png/` の日本語版（`...Japanese (4).png`）は 270×80 と小さく、
英語版と内部の余白が違う別レイアウトだった（ピクセル比較で 17% 相違）。
48px 表示だと高解像度画面でぼけるため、意匠が同じで拡大に強い SVG を採用している。
