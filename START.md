# Как запустить работу в Claude Code (один раз настроить)

## 1. Настройка (PowerShell, один раз)
```powershell
cd $HOME\OneDrive\Desktop\Razrab
git clone https://github.com/a50petr-cmd/demo-sites
cd demo-sites
mkdir .claude\skills -Force
git clone --depth 1 https://github.com/leonxlnx/taste-skill .claude\skills\taste-skill
git clone --depth 1 https://github.com/nextlevelbuilder/ui-ux-pro-max-skill .claude\skills\ui-ux-pro-max
git clone --depth 1 https://github.com/pbakaus/impeccable .claude\skills\impeccable
claude
```
(`.claude/skills/` в .gitignore — скиллы не коммитятся.)

## 2. Промпты по шагам (каждый — в новой сессии или после /clear)
1. `Используй агента ref-hunter для лида gavrilina.` → откройте leads/gavrilina/refs.md, выберите направление А/Б/В.
2. `Используй агента demo-designer для лида gavrilina, направление <буква>.`
3. `Используй агента demo-reviewer для лида gavrilina.` → если вердикт «можно отправлять» — `выложи`.

Модели: ref-hunter и demo-designer — sonnet, demo-reviewer — haiku. Opus не нужен.
