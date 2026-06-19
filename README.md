# 日野町 統計ダッシュボード（プロトタイプ）

[cite_start]滋賀県日野町の公式統計資料「統計でわかる！日野のすがた」のデータを抽出し、視覚的にわかりやすく閲覧できるように構築したオープンデータ利活用のための実証実験プロジェクトです [cite: 1, 2, 3, 8]。

ブラウザ上で軽快に動作するSPA（シングルページアプリケーション）を採用し、トップページでの重要指標（KPI）のハイライト表示や、デジタル庁のダッシュボードデザインガイドラインを参考にした認知負荷の低いUI/UXを目指しています。

## 📊 収録データ一覧

[cite_start]現在、公式資料の目次構成に沿って、以下の25種のデータをCSV形式で `data/` フォルダ内に公開しています。どなたでも自由にダウンロードしてご活用いただけます [cite: 11, 15, 16]。

### 1. 位置・地勢・気象
* [cite_start]**地目別面積** (`hino_land_area.csv`) - 田、畑、宅地、林山などの面積推移 [cite: 96, 98]
* [cite_start]**気象概況** (`hino_weather.csv`) - 令和6年の月別平均気温・降水量 [cite: 108, 109]

### 2. 人口
* [cite_start]**人口・世帯数** (`hino_population.csv`) - 総人口（男女別）および世帯数の推移 [cite: 121, 122]
* [cite_start]**人口動態** (`hino_vital_stats.csv`) - 出生・死亡および転入・転出の推移 [cite: 141, 142]
* [cite_start]**外国人登録者数** (`hino_foreigners.csv`) - 国籍別外国人登録者総数の推移 [cite: 133, 135]
* [cite_start]**産業区分別就業者数** (`hino_industry.csv`) - 第一次〜第三次産業における就業者数の推移 [cite: 161, 163]
* [cite_start]**年齢3区分別人口** (`hino_age.csv`) - 年少・生産年齢・老年人口の割合変化 [cite: 171, 174]

### 3. 産業
* [cite_start]**観光客入込数** (`hino_tourism.csv`) - 日帰り・宿泊別の観光客数の動向 [cite: 200, 202]
* [cite_start]**工業の推移** (`hino_industry_trend.csv`) - 工業事業所数および従業者数の推移 [cite: 209, 211]

### 4. 農林業
* [cite_start]**経営耕地面積** (`hino_farming_area.csv`) - 田、畑、樹園地の面積推移 [cite: 234, 236]
* [cite_start]**農地転用状況** (`hino_farmland_conversion.csv`) - 住宅用地や駐車場などへの転用面積（㎡）推移 [cite: 243, 245]

### 5. 運輸・交通
* [cite_start]**近江鉄道日野駅乗降客数** (`hino_railway.csv`) - 日野駅の年間乗降客数の推移 [cite: 282, 283]
* [cite_start]**町営バス利用状況** (`hino_bus.csv`) - 定期・定期外利用者数の推移 [cite: 274, 275]
* [cite_start]**交通事故発生状況** (`hino_traffic_accident.csv`) - 町内における交通事故件数の推移 [cite: 286, 287]

### 6. 水道・通信・消費
* [cite_start]**上水道給水状況** (`hino_water_supply.csv`) - 給水人口と年間総配水量の推移 [cite: 295, 296]
* [cite_start]**公共下水道整備状況** (`hino_sewerage.csv`) - 下水道の普及率と水洗化率の推移 [cite: 304, 305]
* [cite_start]**ごみ投入量** (`hino_garbage.csv`) - 可燃物および不燃物の排出量トレンド [cite: 335]

### 7. 社会保障
* [cite_start]**国民健康保険** (`hino_nhis.csv`) - 国保被保険者数と加入率の推移 [cite: 363]
* [cite_start]**介護保険** (`hino_nursing_care.csv`) - 第1号被保険者数（前期・後期別）の推移 [cite: 387, 390]
* [cite_start]**保育所・認定こども園** (`hino_childcare.csv`) - 定員および在籍人員の推移 [cite: 409, 411]

### 8. 保健衛生
* [cite_start]**三大疾病別死亡数** (`hino_diseases.csv`) - がん・心疾患・脳血管疾患による死亡数推移 [cite: 418, 419]

### 9. 教育・文化
* [cite_start]**図書館の利用状況** (`hino_library.csv`) - 図書館の来館者数と利用冊数の推移 [cite: 463, 464]
* [cite_start]**文化施設入館者数** (`hino_cultural_facilities.csv`) - 商人館・ふるさと館・感応館の入館者数推移 [cite: 475]

### 10. 財政
* [cite_start]**決算分析指数** (`hino_finance_index.csv`) - 経常収支比率などの健全化指標 [cite: 494, 497]

### 11. 治安・消防
* [cite_start]**火災・救急出動** (`hino_fire_ambulance.csv`) - 火災発生件数と救急車出動件数 [cite: 517, 518]

* **出典:** [日野町公式ウェブサイト「統計でわかる！日野のすがた」](https://www.town.shiga-hino.lg.jp/0000007518.html)

## 💡 外部サイトへの埋め込み

本ダッシュボードは、他のウェブサイトやブログへの埋め込み（iframe）に対応しています。URLの末尾に `?embed=true` を付与すると、ヘッダーや余白が非表示になり、最適化された状態で表示されます。

    <iframe 
        src="https://kken78.github.io/hino-dashboard/?embed=true#population" 
        width="100%" 
        height="500" 
        style="border:none; background:transparent;" 
        scrolling="no">
    </iframe>

※ `#population` の部分を `#tourism` などに変更すると、最初から指定したグラフを開いた状態で表示できます。

## ⚠️ 免責事項

* **データの正確性:** 本リポジトリのCSVデータは、公開されているPDFから独自にテキスト抽出して作成したものです。読み取り誤差や変換ミスが含まれる可能性があるため、正確な数値が必要な公的用途等においては、必ず日野町公式ホームページの元データ（PDF）をご確認ください。
* **位置づけ:** 本プロジェクトは日野町の公式システムではなく、オープンデータ推進に向けた参与による実証実験（プロトタイプ）です。予告なく仕様変更や公開停止を行う場合があります。

## 📄 ライセンス

* **ソースコード:** [MIT License](https://opensource.org/licenses/MIT)
* **公開データ (CSV):** シビックテックの精神に基づき、地域課題の解決や分析等の目的でどなたでも自由にご利用いただけます（CC BY 4.0相当を想定）。