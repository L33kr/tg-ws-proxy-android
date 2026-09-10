# TG WS Proxy Android

Android-версия [TG WS Proxy](https://github.com/Flowseal/tg-ws-proxy) с интерфейсом на Jetpack Compose и нативным прокси-ядром на Rust.

## Возможности

- Локальный MTProto proxy для Telegram
- WebSocket/WSS транспорт
- Cloudflare proxy fallback
- Работа в фоне через Foreground Service
- Просмотр логов в приложении
- Статистика соединений и трафика
- Настройка адреса, порта и пула соединений
- Поддержка пользовательского Cloudflare-домена
- Автозапуск после загрузки Android
- Quick Settings tile
- Material 3 / Material You
- Автоматическая проверка обновлений
- Поддержка ARM64 и ARM32

## Как работает

```text
Telegram Android
        ↓
Local MTProto Proxy (127.0.0.1:1443)
        ↓
TG WS Proxy Android
        ↓
WebSocket / WSS
        ↓
Telegram DC
```

При невозможности подключиться напрямую приложение может использовать Cloudflare fallback.

## Установка

APK можно скачать из раздела Releases.

Для большинства современных Android-устройств используйте ARM64-сборку.

## Сборка

Проект содержит Android-приложение и Rust-библиотеку.

Для сборки Rust-части используется Android NDK и `cargo-ndk`.

На Windows также доступны:

```bat
build_so.bat
build_apk.bat
```

## Лицензия

GPL-3.0.

Основано на [Flowseal/tg-ws-proxy](https://github.com/Flowseal/tg-ws-proxy).
