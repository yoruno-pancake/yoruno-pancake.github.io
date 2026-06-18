# SF6 COMBO MEMO

ストリートファイター6 用のコンボメモ・管理ツールです。技をドラッグ＆ドロップでコンボに組み立て、ダメージ・ドライブゲージ消費・フレーム・ヒット状況・分岐ルートまで記録できます。単一の HTML ファイルで動作し、データはブラウザ内（ローカルストレージ）に保存されます。日本語／English の表示切替に対応しています。

## 📖 使い方ガイド

### 🎮 基本操作

1. 上部プルダウンで使用キャラを選択（**＋ キャラ** で追加、**✎ キャラ名** で名前を変更）
2. PC は左の技リストから右のコンボ枠へ **ドラッグ＆ドロップ**。コンボ内の技もドラッグで並び替え可能で、**ドロップ位置のゴールドの縦線** が挿入先になります（先頭・中間・末尾のどこにでも差し込めます）
3. コンボの **✎ 編集** を押すと編集モードになり、分岐追加・複製・削除・並び替え（▲▼）などが行えます
4. 技カードをクリックでフレームデータ詳細を表示

### 📋 コンボ管理

- **＋ NEW COMBO** — 新しいコンボを追加
- **DMG欄 / DG欄** — ダメージは手動入力。ドライブゲージ消費は自動計算され、**編集中は DG 欄に数値を入れて手動修正** も可能（空欄で自動計算に戻る。OD→OD 派生など自動計算が合わない場合に）
- **FRAME欄** — コンボ終了時の有利/不利フレームを手動入力
- **▲▼ 並び替え** — 編集中に表示順を変更（親子コンボはまとまって移動）
- **技の複製（⧉）** — 編集中、コンボ内の各技にある ⧉ ボタンで、その技の直後に同じ技をもう1つ追加（弱P → 弱P 弱P のように）
- **コンボの複製** — 編集中のコンボを丸ごと複製（**分岐ツリーも一緒に** コピーし、すぐ下に同じ階層で追加）。似た派生の量産に便利
- **📋 コマンド出力** — コンボのコマンドをクリップボードへコピー（外部に貼り付け可）
- **同じ技のまとめ表示** — COMBO LIST / STARTER TREE で同じ技が連続するとき「弱P×3」のようにまとめて表示します（**⚙ 設定** で ON/OFF 切替。**📋 コマンド出力** も同じく「×3」でコピーされます）。**コンボの編集中** は1つずつの表示に戻り、より細かく並び替えできます
- **タグ** — コンボにタグを付けてフィルター

### 🌿 分岐コンボ

- **分岐追加** — 既存コンボから派生ルートを作成。元コンボの **すぐ下** に追加されます
- **↳ 表示** — 親子関係をインデントと矢印で表示
- **差分の色分け** — 親と共通する技は淡色、分岐後の技はオレンジで強調（境目に ⑂ マーク）
- **作成直後** は親と同じ内容なので通常表示のまま「まだ差分がありません」と案内します。技を変更・追加すると、その時点から差分の色分け（⑂）が始まります
- **親の付け替え** — 各コンボ左端の **⠿** を掴んで別コンボの上にドロップ → そのコンボの分岐に変更（**配下のツリーごと** 移動）。一覧の **空き領域** にドロップで **ルートへ** 戻せます
- STARTER TREE でも同じ差分表示で確認できます

### 🎯 ヒット状況（C / PC / D / G）

コンボ内の各技に、当てたときの状況を色付きで記録できます。**✎ 編集** 中、各技チップの **✕ ボタンの手前のボタン** を押すたびに切り替わります（**通常 → C → PC → D → G → 通常** の順で循環）。

- **C** カウンター（黄）— 相手の技に割り込んでヒット
- **PC** パニッシュカウンター（橙）— 確定反撃でヒット
- **D** ディレイ（紫）— 入力を遅らせて繋ぐ技
- **G** ガード（青）— ガードされた（ブロック）状況

設定すると非編集時も技の右側に **バッジ表示** され、**STARTER TREE** や **📋 コマンド出力**（例: 中P(PC)）にも反映されます。**もう一度押して通常** に戻すと解除できます。

### 🔧 技の管理

- **✎ ボタン** — 技のフレームデータを編集
- **＋ 技追加** — 独自の技を新規登録
- **発動条件** — 技に発動条件（例: 体力 25% 以下）を設定でき、設定すると技名の横に ⚡ アイコンが表示されます
- **サムネイル** — 技ごとに 16:9 画像を登録可能
- **ソートバー** — 技タイプ別に技リストを絞り込み
- **技プリセット** — 新規キャラを **＋ キャラ** で追加する際、全キャラ共通の技（立ち・しゃがみ・ジャンプの弱中強 P・K、投げ・ドライブ系、ステップ/歩き/ジャンプ）をまとめて登録するか選べます（通称・フレーム・ダメージは空欄。ドライブ系のゲージ消費のみ設定済み）

### 📑 タブ

- **COMBO LIST** — コンボの作成・編集メイン画面
- **STARTER TREE** — 始動技ごとにコンボをツリー表示
- **📝 MEMO** — キャラごとの自由メモ（個別保存）

### 📱 モバイル表示

- **⚙ 設定** の表示モードで「自動 / PC / モバイル」を切替
- モバイルは編集中の **＋ 技を追加** を押し、技をタップして追加（画面下部のバーで終了）
- **MOVE LIST のヘッダーをタップ** で技リストを折りたたみ、画面を広く使えます
- **≡ メニュー** — ヘッダーの操作ボタン（キャラ追加・技追加・保存・書き出しなど）を折りたたみ/展開できます

### 💾 保存・共有

- **💾 保存** — ブラウザのローカルストレージに保存
- **📤 書き出し** — JSON 形式でエクスポート（外部共有可）
- **📥 読み込み** — JSON ファイルをインポート
- **⚙ 設定** — 表示モード・言語（日本語/English）・**同じ技のまとめ表示** の切替・データ初期化
- **Auto / ±** — 表示サイズの拡大縮小（PC 表示）

---

<details>
<summary>📖 User Guide (English)</summary>

### 🎮 Basics

1. Choose your character from the dropdown at the top (add one with **＋ Character**, rename with **✎ Rename**)
2. On desktop, **drag & drop** a move from the list on the left into a combo slot on the right. Moves inside a combo can also be reordered by dragging — the **gold vertical line at the drop position** shows where it will be inserted (you can drop at the start, middle, or end)
3. Press **✎ Edit** on a combo to enter edit mode, where you can add branches, duplicate, delete, reorder (▲▼), and more
4. Click a move card to view its frame-data details

### 📋 Managing combos

- **＋ NEW COMBO** — Add a new combo
- **DMG / DG fields** — Enter damage manually; Drive Gauge cost is auto-calculated, and **you can override it by typing a number in the DG field while editing** (leave blank to revert to auto — useful when auto-calc is off, e.g. OD→OD derivations)
- **FRAME field** — Manually enter the frame advantage/disadvantage at combo end
- **▲▼ Reorder** — Change the display order while editing (parent/child combos move together)
- **Duplicate a move (⧉)** — While editing, the ⧉ button on each move in a combo inserts another copy of that move right after it (e.g. LP → LP LP)
- **Duplicate a combo** — Copy the combo being edited in full (**including its branch tree**), inserted just below at the same level. Handy for mass-producing similar variants
- **📋 Copy notation** — Copy the combo notation to the clipboard (paste it anywhere)
- **Repeated move display** — In COMBO LIST / STARTER TREE, consecutive identical moves are shown grouped like "LP×3" (toggle ON/OFF in **⚙ Settings**; **📋 Copy notation** is copied with "×3" too). **While editing a combo**, they revert to one-by-one display for finer reordering
- **Tags** — Tag combos and filter by them

### 🌿 Branch combos

- **Add branch** — Create a derived route from an existing combo. It is added **right below** the original
- **↳ display** — Parent/child relationships are shown with indentation and an arrow
- **Diff coloring** — Moves shared with the parent are dimmed; moves after the branch are highlighted in orange (with a ⑂ mark at the split)
- **Right after creation** the branch is identical to its parent, so it stays in normal display with a "no difference yet" notice. Once you change or add a move, diff coloring (⑂) begins from that point
- **Re-parenting** — Grab the **⠿** on the left edge of a combo and drop it onto another combo to make it a branch of that one (**the whole subtree moves with it**). Drop it on **empty space** in the list to send it **back to root**
- The same diff display is also available in STARTER TREE

### 🎯 Hit state (C / PC / D / G)

You can record, in color, the situation in which each move in a combo lands. While in **✎ Edit**, pressing **the button just before the ✕ button** on each move chip cycles it (**Normal → C → PC → D → G → Normal**).

- **C** Counter (yellow) — Hit by interrupting the opponent's move
- **PC** Punish Counter (orange) — Hit as a guaranteed punish
- **D** Delay (purple) — A move linked by delaying the input
- **G** Guard (blue) — The move was guarded (blocked)

Once set, a **badge** also shows on the right of the move outside edit mode, and it carries over to **STARTER TREE** and **📋 Copy notation** (e.g. 中P(PC)). **Press again to return to Normal** to clear it.

### 🔧 Managing moves

- **✎ button** — Edit a move's frame data
- **＋ Move** — Register your own custom move
- **Condition** — Set an activation condition for a move (e.g. HP 25% or below); a ⚡ icon then appears next to the move name
- **Thumbnail** — Register a 16:9 image per move
- **Sort bar** — Filter the move list by move type
- **Move preset** — When adding a new character with **＋ Character**, you can choose to bulk-register the moves common to all characters (standing/crouching/jump light-medium-heavy P・K, throws & Drive moves, step/walk/jump). Nicknames, frames and damage are left blank (only Drive Gauge cost is pre-filled)

### 📑 Tabs

- **COMBO LIST** — The main screen for creating and editing combos
- **STARTER TREE** — Combos shown as a tree grouped by starter move
- **📝 MEMO** — Free notes per character (saved individually)

### 📱 Mobile display

- Switch between "Auto / Desktop / Mobile" via the display mode in **⚙ Settings**
- On mobile, press **＋ Add move** while editing, then tap moves to add them (finish via the bar at the bottom of the screen)
- **Tap the MOVE LIST header** to collapse the move list and use more of the screen
- **≡ Menu** — Collapse/expand the header action buttons (add character, add move, save, export, etc.)

### 💾 Saving & sharing

- **💾 Save** — Save to the browser's local storage
- **📤 Export** — Export as JSON (shareable externally)
- **📥 Import** — Import a JSON file
- **⚙ Settings** — Switch display mode, language (日本語/English) and **repeated move display** / reset data
- **Auto / ±** — Zoom the display in or out (desktop)

</details>
