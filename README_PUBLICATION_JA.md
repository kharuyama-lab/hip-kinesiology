# Hip Kinesiology v1.0 — 公開・更新手順

## 内容
- `index.html`：学生に見せるWeb教材（現行完成版 v1.0、更新可能）
- `.nojekyll`：GitHub Pages用の空ファイル
- `CREDITS_AND_LICENSES.md`：3Dモデルの出典・ライセンス
- `CHANGELOG.md`：更新履歴

**重要**：この配布キットには巨大な3Dモデル `.glb` やThree.js本体は同梱していません。現在の `index.html` は外部配信元から骨・靭帯・筋データとThree.jsを取得します。常時接続が必要で、配信元が停止・変更されるとモデルの読み込みが失敗する可能性があります。大学で長期運用する場合は別途ファイルを適切なライセンスのもとで自サイトへ配置する方法をご検討ください。

## 1. 公開前の教員確認（重要）
1. `index.html` をPCのChrome/Edgeで開いてモデルを読み込みます。
2. 「股関節」「全体」、各運動、筋群、日英表記、タッチ操作が正しく動くことを確認します。
3. 大腿骨頭中心を全学生で固定したい場合は、PCで骨頭中心を確認・調整し、画面の「研究文献・出典・制約」より上にある教員用設定を開き、**「現在の中心を固定した配布用HTMLを生成」**を選びます。
4. ダウンロードされた `HipKinesiology_v1_0_FixedCenter.html` を **`index.html` に改名して、このキットの `index.html` と置き換えます。** この操作により全端末で同じ回転中心設定が使われます。
5. 固定中心を書き出さない場合は元の自動推定・端末の保存値が使われるため、全学生で統一した中心になる保証はありません。

## 2. GitHub Pages（個人GitHubアカウント、無料の公開リポジトリを使用）
1. https://github.com/ にサインインし、`New repository` から `hip-kinesiology` という **Public** リポジトリを作ります。大学の正式サイトまたはアクセス制御が必要な場合は、大学のWeb管理者と確認してください。
2. `Add file` → `Upload files` を選び、このフォルダ内の `index.html`、`CREDITS_AND_LICENSES.md`、`CHANGELOG.md` をアップロードし、変更を保存（Commit changes）します。`.nojekyll` は隠しファイルなのでアップロードできなくても必須ではありません。
3. リポジトリの `Settings` → `Pages` → `Build and deployment` → `Source: Deploy from a branch` → `Branch: main`、`/(root)` → `Save` を選びます。
4. 公開後のURLは通常 `https://<GitHubユーザー名>.github.io/hip-kinesiology/` です。**公開した実URLをGitHubのSettings → Pagesで確認**してください。GitHubユーザー名とリポジトリ名を変更するとURLも変わります。
5. 公開したURLをPC、スマホ、タブレットで開いて、3D表示とドラッグ・ピンチ・タップで組織名が出ることを確認します。
6. 正しく動いたら、確定したURLからQRコードを生成して、授業スライド・LMSで配布します。URLが決まる前にはQRコードを生成しません。

公式手順：
- https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site
- https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

## 3. 更新してもURLは維持できます
1. 新しいHTMLで動作確認し、必要なら回転中心を固定して書き出します。
2. **同じリポジトリ、同じ階層の `index.html` を新ファイルで置換**し、GitHub上でコミットします。
3. 公開反映を確認します。URLとQRコードは変更不要です。ブラウザで旧版が表示される場合は再読み込みしてください。
4. `CHANGELOG.md` に修正内容・日付・改訂版番号を記録します。以前の版はGitの履歴から戻せます。

## 4. 学生端末の条件
- PC：Chrome / Edge / Safari等のWebGL2対応ブラウザ。マウス／トラックパッド
- タブレット：iPadOS SafariまたはAndroid Chrome等。タップ選択、1本指回転、ピンチ拡大縮小
- スマホ：同上。狭い画面では左上の「操作パネル」を開き、閉じると3D画面が広く使えます
- インターネット接続が必要。初回読込に時間がかかる場合があります。端末のRAM/GPUやブラウザ設定によっては表示できない場合があります
- インストール・サインインは学生側には不要。教員PCは起動し続ける必要なし

授業前に**iPhone、Android、iPad、Windows/Macの少なくとも各1台**で実機確認し、大学のWi-Fiとモバイル回線でも動作を確認してください。授業中の通信不調に備え、講義用PCに正常動作した版を保存し、必要に応じて画面録画も用意してください。

## 5. 公開・利用上の注意
- GitHub Pagesのサイトは一般公開されます。学内限定公開が必要な場合は大学の認証付きサーバーやLMS対応を検討してください。
- 解剖モデル由来のライセンス・帰属表示を削除しないでください。詳しくは `CREDITS_AND_LICENSES.md` を参照してください。
- 靭帯の緊張や筋短縮表示は授業目的の模式表現で、個人の筋活動や組織張力を測定したものではありません。
- `index.html` を手元で開いて動くことと、公開URLで動くことは別です。公開後に必ず実機で確認してください。

## 6. 公開前チェック
- [ ] 骨・靭帯・筋がすべて読み込まれる
- [ ] 日本語名／英語名が表示され、英語名の末尾に `.r` / `.l` がない
- [ ] 股関節の回転中心・屈伸・内外転・内外旋の方向が正しい
- [ ] 靭帯ハイライトと筋群プリセットが授業内容に対応する
- [ ] スマホで「操作パネル」の開閉、3D回転、タップ選択が可能
- [ ] iPad/Androidタブレットでタップ・ピンチが可能
- [ ] 公開URLからアクセスでき、QRコードが同じURLを開く
- [ ] 著作権・ライセンス表記が残っている
