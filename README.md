# TG WS Proxy Android

Android-форк оригинального проекта [Flowseal/tg-ws-proxy](https://github.com/Flowseal/tg-ws-proxy) — локального MTProto-прокси для Telegram с WebSocket/WSS-транспортом и Cloudflare fallback.

## Возможности

- Android UI на Kotlin / Jetpack Compose / Material 3
- Нативное прокси-ядро на Rust
- Foreground Service для фоновой работы
- Логи и статистика работы прокси
- Material You / динамические темы
- Автозапуск после загрузки
- Quick Settings tile
- Проверка обновлений через GitHub Releases
- Cloudflare fallback и пользовательский CF-домен
- ARM64 / ARM32 / Universal сборки

## Принцип работы

```text
Telegram Android
    ↓
MTProto proxy 127.0.0.1:1443
    ↓
TG WS Proxy Android
    ↓
WSS / Cloudflare / Direct
    ↓
Telegram DC
```

## Установка

Скачайте APK из раздела Releases и установите его на Android.

Для большинства современных устройств подходит ARM64-сборка.

## Сборка

Для Android используется Gradle, для нативной части — Rust + Android NDK / cargo-ndk.

На Windows доступны скрипты:

```bat
build_so.bat
build_apk.bat
```

## Лицензия

GPL-3.0.

Оригинальный проект: [Flowseal/tg-ws-proxy](https://github.com/Flowseal/tg-ws-proxy)
