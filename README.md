# Веб рація

## Опис

"Веб рація" — це веб-додаток, який дозволяє користувачам здійснювати голосові дзвінки через браузер. Додаток використовує WebRTC для запису аудіо та Socket.IO для реального часу передачі даних між клієнтами, а також для синхронізації статусу користувачів. Цей проект корисний для розробників та користувачів, які хочуть створити або скористатися веб-додатком для голосових комунікацій без необхідності встановлювати додаткове програмне забезпечення.

<p align="center">
  <img src="wrs.png" alt="Web Radio" />
</p>

## Особливості

- **Веб-додаток** для голосових дзвінків через браузер.
- **Підтримка реального часу** за допомогою Socket.IO для передачі аудіо та синхронізації статусу.
- Використовує **WebRTC** для доступу до мікрофону та запису аудіо.
- Аудіо записується та зберігається на сервері у форматі WAV.
- Індикація стану користувача через кольорові індикатори (зелений для готовності, червоний для запису, жовтий для відтворення аудіо).
- Підтримка одночасної комунікації декількох користувачів.

## Технології

- **Node.js** — серверна платформа для обробки запитів.
- **Socket.IO** — бібліотека для реального часу комунікацій між клієнтом та сервером.
- **Express** — веб-фреймворк для Node.js.
- **WebRTC** — технологія для обміну мультимедійними даними в реальному часі.
- **MediaRecorder API** — для запису аудіо з мікрофону користувача.

## Структура проекту

```
wrs
├─ README.md
├─ audio_recordings
├─ package-lock.json
├─ package.json
├─ public
│  ├─ client.js
│  ├─ index.html
│  └─ styles.css
└─ server.js
```

### Пояснення файлів:

- **server.js** — серверна частина на Node.js, що обробляє запити та комунікацію через Socket.IO. Зберігає записані аудіофайли та передає їх клієнтам.
- **public/index.html** — HTML-сторінка, що містить інтерфейс для користувача.
- **public/styles.css** — стилі для інтерфейсу.
- **public/client.js** — JavaScript, що відповідає за взаємодію на стороні клієнта, обробку аудіо та комунікацію з сервером.
- **audio_recordings/** — директорія для збереження аудіофайлів.

## Як запустити проект

1. **Клонування репозиторію:**

   ```bash
   git clone https://github.com/yourusername/wrs.git
   cd wrs
   ```

2. **Інсталяція залежностей:**

   Використовуйте npm для встановлення всіх необхідних пакетів:

   ```bash
   npm install
   ```

3. **Запуск сервера:**

   Для запуску сервера на локальній машині використовуйте команду:

   ```bash
   npm start
   ```

   Сервер запуститься на порту 3000 або на порту, заданому в змінній середовища `PORT`.

4. **Відкриття додатку в браузері:**

   Відкрийте браузер та перейдіть за адресою:

   ```
   http://localhost:3000
   ```
