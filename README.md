# TG WS Proxy for Android

Android порт [Flowseal/tg-ws-proxy](https://github.com/Flowseal/tg-ws-proxy) с графическим интерфейсом и нативным Rust-ядром.

## О приложении

TG WS Proxy Android запускает локальный MTProto-прокси на Android и перенаправляет трафик Telegram через WebSocket/WSS. Это позволяет использовать тот же подход, что и оригинальный TG WS Proxy, непосредственно на телефоне.

Приложение состоит из двух частей:

- Android UI на Kotlin / Jetpack Compose / Material 3;
- нативное прокси-ядро на Rust, подключённое через JNA.

## Возможности

- локальный MTProto-прокси;
- WebSocket/WSS транспорт;
- Cloudflare proxy fallback;
- пользовательский Cloudflare-домен;
- поддержка ARM64 и ARM32;
- Foreground Service;
- просмотр логов;
- статистика работы прокси;
- запуск после загрузки устройства;
- Quick Settings tile;
- Material You / динамические цвета;
- встроенная проверка обновлений через GitHub Releases.

## Архитектура

```text
Telegram Android
        ↓
MTProto proxy 127.0.0.1:1443
        ↓
TG WS Proxy Android
        ↓
WebSocket / WSS
        ↓
Telegram DC
```

При проблемах прямого WebSocket-соединения приложение может использовать Cloudflare fallback.

## Установка

Готовые APK доступны в разделе Releases.

Для большинства современных телефонов используется ARM64-сборка (`arm64-v8a`). Для старых устройств доступна ARM32 (`armeabi-v7a`).

## Сборка

### Rust

Для сборки нативной библиотеки нужен Rust и Android NDK.

На Windows можно использовать:

```bat
build_so.bat
```

### Android APK

```bat
build_apk.bat
```

Также проект можно открыть в Android Studio и собрать стандартными Gradle-задачами.

## Лицензия

Проект распространяется под GPL-3.0.

Оригинальный проект: [Flowseal/tg-ws-proxy](https://github.com/Flowseal/tg-ws-proxy)
