# MeditationApp

## Статус
Прототип

## Описание
Android-приложение для медитаций, расслабления и дыхательных практик.

## Технологии
Kotlin + Jetpack Compose + Gradle Kotlin DSL.

## GitHub
https://github.com/appdepp/MeditationApp

## Локальный путь
/Users/oleksandrtkachenko/Documents/Codex/2026-06-22/codex-windsurf-cursor-github-copilot-agent/MeditationApp

## Сборка
./gradlew assembleDebug

## Техническое задание
TECH_SPEC.md

## APK
app/build/outputs/apk/debug/app-debug.apk

## Текущее состояние
Есть главный экран в светлых сиренево-фиолетовых тонах, стиль ближе к раннему glossy Apple.
Есть дыхательный круг. Тап по кругу запускает сессию. Повторный тап останавливает и сбрасывает сессию. Паузы быть не должно.
Есть выбор сессии:
- Morning clarity — 5 min
- Deep focus — 12 min
- Sleep wind-down — 20 min

Есть выбор звука в виде прокручиваемого picker-окна, не плитками.
Звуковые режимы:
- Focus
- Relax
- Reset
- Harmony
- Grounding
- Clarity
- Sleep

Текущее приложение генерирует звук в коде через Android AudioTrack.
Целевое решение по ТЗ: основной звук должен идти из локальных MP3-фонов, а частоты должны остаться тихим слоем примерно 25% от основного звука.

Целевые MP3-фоны:
- Forest
- Rain
- River
- Ocean
- Wind
- City
- Grass
- Buddha Temple

Также нужен отдельный MP3-файл мужского голосового сопровождения для Session 1:
- Спокойное дыхание — 1 минута
- Рекомендуемое имя: voice_session_calm_breath_1_min_male.mp3
- Голос запускается вместе с сессией и останавливается/сбрасывается вместе с дыхательным кругом.

## Важные правила
Перед изменениями:
git status --short --branch

После изменений:
./gradlew assembleDebug

Если сборка успешна:
git add .
git commit -m "..."
git push

Не коммитить:
- build/
- .gradle/
- local.properties
- APK-файлы
