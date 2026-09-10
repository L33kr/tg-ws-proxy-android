# TG WS Proxy Android

Это Android-форк оригинального проекта [Flowseal/tg-ws-proxy](https://github.com/Flowseal/tg-ws-proxy) — локального MTProto-прокси для Telegram, который использует WebSocket/WSS-транспорт и Cloudflare fallback.

## Возможности

- Android UI на Kotlin + Jetpack Compose + Material 3
- Нативное прокси-ядро на Rust
- Foreground Service для стабильной фоновой работы
- Просмотр логов прямо в приложении
- Динамические темы Material You
- Автозапуск и быстрый доступ через системную плитку
- Обновление приложения через GitHub Releases
- Cloudflare fallback / custom CF domain
- Настройка локального адреса и порта
- Поддержка ARM64, ARM32 и universal APK

## Как это работает

```text
Telegram Android
    ↓
локальный MTProto proxy (127.0.0.1:1443)
    ↓
TG WS Proxy
    ↓
WSS / Cloudflare или прямое соединение
    ↓
Telegram DC
```

## Установка

Скачайте APK из раздела Releases и установите его на Android.

Для большинства современных устройств подходит ARM64-сборка.

## Использование

1. Запустите приложение.
2. Нажмите запуск прокси.
3. Настройте Telegram на локальный MTProto-прокси `127.0.0.1:1443`.
4. При необходимости настройте Cloudflare fallback в параметрах приложения.

## Сборка

Для Android-части используется Gradle, а нативное ядро собирается Rust/cargo-ndk.

Смотрите `build_apk.bat` и `build_so.bat` для локальной сборки на Windows.

## Происхождение проекта

Проект является Android-портом/форком [Flowseal/tg-ws-proxy](https://github.com/Flowseal/tg-ws-proxy).

## Лицензия

GPL-3.0.
