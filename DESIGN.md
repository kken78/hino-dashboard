# DESIGN.md

このリポジトリ（日野のすがた）の設計の決定を記録する。ポータル全体に共通の決まりは hino-portal の DESIGN.md による。食い違うときは hino-portal の DESIGN.md を先に直し、このリポジトリをそれに合わせる。

## 設計の決定

### ADR-1 共通の部品は hino-portal の正本を写し、CI で確かめる（2026-11-07）

状態：決定

背景：hino-portal DESIGN.md 9.2 の段階1で、ポータルの下のページの共通の見出し・分野のナビ・ページの一覧・フッター・`<title>` をそろえることになった（hino-portal DESIGN.md 2章・9.1）。

決定：

1. 共通の部品（見出し・分野のナビ・ページの一覧・フッター）は、hino-portal の `shared/` の正本（shell.css・header.html・siblings-stat.html・footer.html）を `index.html` に写す。写した部分は `<!-- portal-shared:〈名前〉 start -->` と `<!-- portal-shared:〈名前〉 end -->` で囲む。
2. 写した部分は手で変えない。変えるときは hino-portal の正本を先に変え、それを写し直す。ページごとに変えるのは、いまの分野・ページの印（`aria-current="page"`）と、フッターの `{{…}}` の中身だけとする。
3. 写したものが正本と同じかは、CI（`.github/workflows/check-shared.yml`）で hino-portal を浅く取ってきて `python3 hino-portal/shared/check.py index.html` で確かめる。
4. ページの構造（共通の見出し、ページの見出し、分野の中のページの一覧、本文、フッター）は hino-portal DESIGN.md 2章による。このページの分野は「統計とくらし」、ページの題は「日野のすがた」とする。
5. この段階では、ページの色・文字の大きさ・グラフは変えない（hino-portal DESIGN.md 9.2 の段階2以降）。
