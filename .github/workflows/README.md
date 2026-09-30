# NEXUS Game Space — Native Android APK

Премиальный игровой центр производительности (уровень Xiaomi Game Turbo / ASUS Game Space).

Портировано из веб-прототипа NEXUS в нативный Android-проект.

## Возможности

- **Game Hub** — красивая сетка игр с иконками и быстрым запуском
- **4 режима**: Extreme / Stable FPS / Endurance / Competitive
- **Очистка RAM** + убийство фоновых процессов
- **Игровой оверлей** (FPS, температура, CPU/GPU, RAM, пинг)
- **Do Not Disturb** + блокировка случайных касаний
- **Сетевой буст** (DNS / Wi-Fi lock)
- **Продвинутые настройки** (Root): губернаторы CPU, частоты, I/O, thermal
- **Полная локализация** RU + EN
- Тёмная неоновая тема

## Структура проекта

```
NEXUS-GameSpace/
├── app/src/main/
│   ├── AndroidManifest.xml
│   ├── java/com/nexus/gamespace/
│   │   ├── MainActivity.java
│   │   ├── HubFragment.java
│   │   ├── LibraryFragment.java
│   │   ├── LabFragment.java
│   │   ├── OverlayService.java
│   │   ├── BoostService.java
│   │   ├── RootHelper.java
│   │   ├── GameDetector.java
│   │   ├── ProfileManager.java
│   │   ├── models/ (Game, Profile, Mode...)
│   │   └── utils/
│   └── res/
│       ├── layout/
│       ├── values/ + values-ru/
│       └── drawable/
└── docs/BUILD.md
```

## Как собрать APK (только на телефоне)

### Вариант A — Sketchware Pro (рекомендуется)

1. Установи **Sketchware Pro** (или Sketchware IA) из официального источника.
2. Создай новый проект:
   - Package: `com.nexus.gamespace`
   - Min SDK: 26, Target: 34
3. Скопируй все `.java` файлы в Java-секцию проекта.
4. Создай layouts по XML из папки `res/layout`.
5. Добавь строки из `values` / `values-ru`.
6. В манифесте добавь разрешения и сервисы (см. AndroidManifest.xml).
7. Нажми **Build → Export Signed APK**.

### Вариант B — Pocket Studio

1. Открой Pocket Studio.
2. Импортируй всю папку `NEXUS-GameSpace` как Gradle-проект (или создай новый и скопируй исходники).
3. Build → APK.

Подробные шаги — в `docs/BUILD.md`.

## Важно

- Без Root работают: профили, оверлей, очистка RAM, DND, сетевой буст.
- С Root открываются: губернаторы, частоты CPU/GPU, I/O scheduler, снятие thermal throttling.
- Приложение **не** является malware и не держит постоянные фоновые сервисы.
