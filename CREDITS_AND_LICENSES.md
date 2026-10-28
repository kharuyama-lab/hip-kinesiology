# 使用データ・クレジット（学生向け教材）

本教材は教育用のブラウザベース3D股関節学習ツールであり、外部提供の3DモデルとThree.jsを読み込みます。

## 3Dモデル
- **BodyParts3D — The Database Center for Life Science (DBCLS)**：オリジナルの解剖学的形状。Z-Anatomy のライセンス・クレジットにおける表記は **CC BY-SA 2.1 Japan**。
- **Z-Anatomy — The libre 3D atlas of anatomy**：解剖学的形状の加工・追加。**CC BY-SA 4.0**。
- **nqwrc/3d-anatomy**：Z-Anatomy系モデルをGLBとして公開した3D Anatomyプロジェクト。https://github.com/nqwrc/3d-anatomy

**注意：** nqwrc/3d-anatomy全体の配布ライセンスは **CC BY-NC-SA 4.0** と表明されています（腎臓・内耳の非商用制限付きデータを含むため）。本教材は骨・筋・関節等の3つのGLBを外部読込しています。別サーバーへモデルを複製・再配布する場合は、元の `LICENSE`、`NOTICE`、および `public/models/License.txt` を確認・保持してください。商用使用や公開範囲が異なる場合の確認が必要です。

情報源：
- https://github.com/nqwrc/3d-anatomy/blob/master/LICENSE
- https://github.com/nqwrc/3d-anatomy/blob/master/NOTICE
- https://github.com/nqwrc/3d-anatomy/blob/master/public/models/License.txt
- https://github.com/Z-Anatomy/Models-of-human-anatomy/blob/master/License.txt
- https://creativecommons.org/licenses/by-nc-sa/4.0/
- https://creativecommons.org/licenses/by-sa/4.0/

## Web描画
- Three.js 0.160.0、GLTFLoader、DRACOLoader： https://threejs.org/
- ソフトウェアに適用されるライセンスは元ソース（MIT等）を確認してください。

## 教育用モデルの特徴
靭帯の緊張・弛緩、筋短縮・伸長、筋膜の追従は授業内容を説明する**模式的な表示**であり、力学解析や測定値とは異なります。モデル内部識別子の右側 `.r` と左側 `.l` は、英語ポップアップから除去していますが、データ識別用の内部名称は変更していません。

更新日：2026-10-28
