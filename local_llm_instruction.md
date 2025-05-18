حق با توئه! در پاسخ قبلی فقط محتوا رو به صورت Markdown آورده بودم ولی صرفاً داخل یک بلاک کد ` ```markdown ` گذاشتم که باعث شد قالب فایل کامل به نظر نرسه یا تفکیک بخش‌ها به‌خوبی مشخص نباشه.

در ادامه، فایل `README.md` به صورت کامل، تمیز و با رعایت اصول Markdown استاندارد آماده شده:

---

# 🧠 راه‌اندازی هوش مصنوعی شخصی (آفلاین + رایگان)

این پروژه به شما کمک می‌کند تا بدون نیاز به اینترنت، یک مدل هوش مصنوعی پیشرفته مانند **Qwen 8B** را روی سیستم شخصی خود اجرا کنید، با حفظ کامل **حریم خصوصی**.

## 💻 پلتفرم‌های پشتیبانی‌شده

* ✅ Windows
* ✅ macOS

## 🔧 ابزارهای مورد نیاز

* [Ollama](https://ollama.com) – اجرای مدل‌های هوش مصنوعی به‌صورت محلی
* [Docker + Open WebUI](https://github.com/open-webui/open-webui) – رابط گرافیکی سبک برای چت با مدل‌ها
* [Anaconda / Miniconda](https://www.anaconda.com/products/distribution) – محیط مدیریت شده Python برای نصب آسان‌تر

---

## 🖥 آموزش نصب در ویندوز

### 🅰 نصب با Anaconda / Conda

1. نصب Anaconda از [لینک رسمی](https://www.anaconda.com/products/distribution)
2. باز کردن **Anaconda Prompt** و اجرای دستورات زیر:

   ```bash
   conda create -n ollama python=3.10 -y
   conda activate ollama
   pip install ollama
   ollama server start
   ollama run qwen:8b
   ```

### 🅱 نصب مستقیم با Installer

1. دانلود Ollama از [https://ollama.com](https://ollama.com)
2. نصب فایل `.exe` و اجرای آن
3. اجرای مدل در CMD یا PowerShell:

   ```bash
   ollama run qwen:8b
   ```

### 🅲 نصب رابط گرافیکی Open WebUI با Docker

1. نصب [Docker Desktop for Windows](https://www.docker.com/products/docker-desktop)

2. اجرای دستورات زیر:

   ```bash
   docker pull ghcr.io/open-webui/open-webui:main

   docker run -d ^
     -p 3000:3000 ^
     -v open-webui:/app/backend/data ^
     --add-host=host.docker.internal:host-gateway ^
     --name open-webui ^
     --restart always ^
     ghcr.io/open-webui/open-webui:main
   ```

3. باز کردن مرورگر و رفتن به آدرس:

   ```
   http://localhost:3000
   ```

---

## 🍏 آموزش نصب در macOS

### 🅰 نصب با Anaconda / Conda

1. نصب Anaconda از [لینک رسمی](https://www.anaconda.com/products/distribution)
2. باز کردن **Terminal** و اجرای دستورات زیر:

   ```bash
   conda create -n ollama python=3.10 -y
   conda activate ollama
   pip install ollama
   ollama server start
   ollama run qwen:8b
   ```

### 🅱 نصب مستقیم با Installer

1. دانلود Ollama از [https://ollama.com](https://ollama.com)
2. اجرای فایل `.pkg` و نصب آن
3. اجرای مدل در ترمینال:

   ```bash
   ollama run qwen:8b
   ```

### 🅲 نصب رابط گرافیکی Open WebUI با Docker

1. نصب [Docker Desktop for Mac](https://www.docker.com/products/docker-desktop)

2. اجرای دستورات زیر در ترمینال:

   ```bash
   docker pull ghcr.io/open-webui/open-webui:main

   docker run -d \
     -p 3000:3000 \
     -v open-webui:/app/backend/data \
     --add-host=host.docker.internal:host-gateway \
     --name open-webui \
     --restart always \
     ghcr.io/open-webui/open-webui:main
   ```

3. باز کردن مرورگر و رفتن به:

   ```
   http://localhost:3000
   ```

---

## 💡 نکات مهم

* ⏱ اجرای اولیه مدل ممکن است چند دقیقه طول بکشد (برای دانلود مدل).
* 🔒 مدل‌ها به‌صورت **آفلاین** و **بدون ارسال اطلاعات به سرور خارجی** کار می‌کنند.
* 🧠 مدل‌های جایگزین: `llama3`, `mistral`, `gemma` و دیگران.
* ⚙️ قابلیت استفاده در Agentهای خودکار برای اجرای دستورات پیچیده (با آموزش‌های آتی).

---

## 📬 پشتیبانی

اگر در مراحل نصب یا اجرا مشکلی دارید، لطفاً در بخش [Issues](https://github.com/your-repo/issues) گزارش دهید یا در Discussions شرکت کنید.

---

## 📝 لایسنس

این آموزش متن‌باز است، اما برای استفاده از مدل‌ها و ابزارهای جانبی لطفاً قوانین و لایسنس‌های هر ابزار را بررسی کنید.

---

آیا مایلی این فایل رو به صورت `.md` برایت خروجی بدم تا مستقیماً استفاده یا آپلودش کنی؟
