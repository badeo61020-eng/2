## Skills
A skill is a set of local instructions to follow that is stored in a `SKILL.md` file. Below is the list of skills that can be used. Each entry includes a name, description, and file path so you can open the source for full instructions when using a specific skill.
### Available skills
- natural-background-recompose: Nano Banana Pro等で人物や商品の背景を差し替える際に、貼り込み感（切り抜き感・浮き・輪郭ハロ・光不一致）を抑えて自然に再生成するためのスキル。道路に限らず、屋内外の任意背景へ柔軟に適用したいときに使う。 (file: C:/Users/shins/.codex/skills/natural-background-recompose/SKILL.md)
- inorganic-gray-wall-model-metaprompt: 無機質なグレー調の長い壁前で、モデル撮影風画像作成用のメタプロンプトを作成・調整するスキル。メンズ訴求時の男性固定とバッグサイズ感固定が必要なときに使う。 (file: C:/Users/shins/.codex/skills/inorganic-gray-wall-model-metaprompt/SKILL.md)
- cafe-register-payment-recompose: カフェのレジ前で「現金を取り出し途中（未受け渡し）」の画像を、参照画像の人物・手・バッグ同一性を維持しつつ背景差し替え感なく再構図で生成するためのスキル。レジ文脈が弱い、単なる背景置換になる、現金を渡し済みにしてしまう場合に使う。 (file: skills/cafe-register-payment-recompose/SKILL.md)
- curtain-rail-end-cap-nanobanana: Nano Banana Proでカーテンレール端部のエンドキャップを追加・差し替え・反転・嵌合補正するときの専用スキル。参考画像の背面/側面統合、サイズ補正、自然な嵌合が必要なときに使う。 (file: skills/generic/curtain-rail-end-cap-nanobanana/SKILL.md)
- skill-creator: Guide for creating effective skills. This skill should be used when users want to create a new skill (or update an existing skill) that extends Codex's capabilities with specialized knowledge, workflows, or tool integrations. (file: C:/Users/shins/.codex/skills/.system/skill-creator/SKILL.md)
- skill-installer: Install Codex skills into $CODEX_HOME/skills from a curated list or a GitHub repo path. Use when a user asks to list installable skills, install a curated skill, or install a skill from another repo (including private repos). (file: C:/Users/shins/.codex/skills/.system/skill-installer/SKILL.md)
### How to use skills
- Discovery: The list above is the skills available in this session (name + description + file path). Skill bodies live on disk at the listed paths.
- Trigger rules: If the user names a skill (with `$SkillName` or plain text) OR the task clearly matches a skill's description shown above, you must use that skill for that turn. Multiple mentions mean use them all. Do not carry skills across turns unless re-mentioned.
- Missing/blocked: If a named skill isn't in the list or the path can't be read, say so briefly and continue with the best fallback.
- How to use a skill (progressive disclosure):
  1) After deciding to use a skill, open its `SKILL.md`. Read only enough to follow the workflow.
  2) When `SKILL.md` references relative paths (e.g., `scripts/foo.py`), resolve them relative to the skill directory listed above first, and only consider other paths if needed.
  3) If `SKILL.md` points to extra folders such as `references/`, load only the specific files needed for the request; don't bulk-load everything.
  4) If `scripts/` exist, prefer running or patching them instead of retyping large code blocks.
  5) If `assets/` or templates exist, reuse them instead of recreating from scratch.
- Coordination and sequencing:
  - If multiple skills apply, choose the minimal set that covers the request and state the order you'll use them.
  - Announce which skill(s) you're using and why (one short line). If you skip an obvious skill, say why.
- Context hygiene:
  - Keep context small: summarize long sections instead of pasting them; only load extra files when needed.
  - Avoid deep reference-chasing: prefer opening only files directly linked from `SKILL.md` unless you're blocked.
  - When variants exist (frameworks, providers, domains), pick only the relevant reference file(s) and note that choice.
- Safety and fallback: If a skill can't be applied cleanly (missing files, unclear instructions), state the issue, pick the next-best approach, and continue.

## File Delivery Rule
- When creating or opening a user-facing Markdown or document file, always include both the file path and its containing folder path in the response.
- Always write the containing folder path as a full absolute path, not only a folder name or relative path.
- When the user explicitly asks to display a newly created Markdown or document file on Windows, create/save the file first and then open that exact file automatically if permissions allow.
- When creating a new prompt file for the user, always save the file first and then open that exact file automatically on Windows if permissions allow, so it appears in the sidebar without requiring an extra request.



