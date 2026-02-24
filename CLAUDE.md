# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Purpose

This repository is a memo/template collection for Claude Code agent operations. It stores reusable prompts and configuration templates to be applied when setting up or operating Claude Code in other projects.

## File Conventions

- **`prompt`** — Plain text prompt files (no extension) containing multi-step agent instructions
- **`*_prompt.md`** — Markdown-formatted prompt templates (e.g., `claudeignore_prompt.md`)

New prompts should follow one of these two conventions depending on whether markdown formatting is needed.

## Contents

### `prompt`
A 4-step process prompt for "Context Standardization & Agent Architecture Setup". When applied to a target project, it:
1. Renames misnamed files (e.g., `Claude.md`) to `CLAUDE.md`
2. Analyzes whether the project has the recommended agent architecture (`README.md`, `CLAUDE.md`, `TODO.md`, `agents/*.md`, `rules/*.md`)
3. Appends "Core Instructions" to `CLAUDE.md` if missing (document sync, single source of truth, `TODO.md` state management, rule adherence)
4. Verifies the resulting structure with `ls -F` and `cat CLAUDE.md`

### `claudeignore_prompt.md`
A ready-to-use `.claudeignore` template covering 8 categories: dependencies, lock files, build artifacts, secrets, logs, binaries/media, IDE metadata, and `.git/`.

## Core Instructions

- **ドキュメントの同期**: 仕様、機能、アーキテクチャに変更を加えた際は、必ず `README.md` を更新してください。
- **知識の源泉**: プロジェクトの仕様やセットアップ手順は `README.md` を正（Single Source of Truth）とします。
- **状態管理**: 進捗状況は常に `TODO.md` を参照し、タスク完了時に必ずチェックを入れ、次のタスクを明確にしてください。
- **ルール厳守**: 特定の実装詳細については `rules/*.md` に従ってください。
