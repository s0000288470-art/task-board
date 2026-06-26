# Task Board Project

## Project Overview

A task board application for managing tasks visually (Kanban-style or similar).

## Tech Stack

- **React 19** — UI ライブラリ
- **Vite 8** — ビルドツール / 開発サーバー
- **CSS Modules なし** — コンポーネントごとに `.css` ファイルを分けて plain CSS で記述
- **localStorage** — タスクの永続化

## Component Naming Conventions

- コンポーネントファイルは PascalCase: `App.jsx`, `TaskItem.jsx`
- コンポーネント関数は PascalCase の default export: `export default function App()`
- CSS クラス名は kebab-case: `.task-item`, `.add-btn`
- イベントハンドラは `handle` プレフィックス: `handleKeyDown`、または動詞のみ: `addTask`, `toggleTask`, `deleteTask`

## Project Structure

```
task-board/
├── src/
│   ├── main.jsx      # エントリポイント
│   ├── App.jsx       # ルートコンポーネント
│   ├── App.css       # App のスタイル
│   └── index.css     # グローバルスタイル
├── index.html
└── vite.config.js
```

## Deploy

- **本番 URL**: https://s0000288470-art.github.io/task-board/
- **方法**: `main` ブランチへのプッシュで GitHub Actions が自動ビルド・デプロイ
- **設定ファイル**: `.github/workflows/deploy.yml`
- Vite の `base` は `/task-board/` に設定済み

## Development Guidelines

- Write clean, minimal code without unnecessary comments or abstractions.
- Do not add error handling or validation beyond what is explicitly required.
- Prefer editing existing files over creating new ones.
- Do not create documentation files unless explicitly requested.

## Git Operation Rules

**Every time code is changed, commit and push to GitHub immediately.**

### Workflow

1. Make the code change.
2. Stage only the relevant files (never `git add -A` blindly — exclude `.env`, secrets, and large binaries).
3. Write a concise commit message focused on *why*, not *what*.
4. Push to the remote branch.

```bash
git add <specific-files>
git commit -m "short description of why this change was made"
git push
```

### Commit Message Style

- Use the imperative mood: "Add login page", "Fix task drag bug", "Remove unused dependency"
- Keep the subject line under 72 characters.
- No period at the end of the subject line.

### Branch Strategy

- `main` — always deployable; never force-push.
- Feature work goes on a topic branch; open a PR to merge into `main`.

### What NOT to commit

- `.env` files or any file containing secrets or credentials.
- Large binary files or build artifacts (`node_modules/`, `dist/`, `.next/`, etc.).
- Editor-specific files unless already in `.gitignore`.
