# Oleg's Art Gallery / Галерея рисунков Олега

![Preview](images/preview.png) <!-- optional: remove if no preview -->

A simple static website to showcase drawings by 10-year-old Oleg.  
Built with pure HTML and CSS — no frameworks. Easy to run and containerize.  
Made by Oleg with help from his dad.

Простой статический сайт для демонстрации рисунков 10-летнего Олега.  
Сделан на чистом HTML и CSS — без фреймворков. Легко запускать и упаковывать в Docker.  
Создан Олегом при поддержке папы.

---

## 📁 Project structure / Структура проекта

.
├── index.html          # Main page
├── style.css           # Styling (optional, if used)
├── images/             # Folder with Oleg's drawings
│   ├── drawing1.jpg
│   ├── drawing2.png
│   └── ...
└── README.md


## ▶️ How to run / Как запустить

### Locally / Локально

Just open `index.html` in your browser.  
Просто откройте `index.html` в браузере.

### With Python (optional) / С помощью Python (опционально)

```bash
cd /path/to/project
python3 -m http.server 8000

Then open http://localhost:8000.
With Docker / В Docker

docker build -t olegs-art .
docker run -d -p 8080:80 --name oleg-gallery olegs-art

Then open http://localhost:8080.

    Note: Make sure your Dockerfile copies index.html and the images/ folder into /usr/share/nginx/html (or your web server root).

📦 Dockerfile example (optional)

If you don't have one yet:

FROM nginx:alpine
COPY index.html /usr/share/nginx/html/
COPY images/ /usr/share/nginx/html/images/

Made with ❤️ by Oleg and his dad.
Сделано с ❤️ Олегом и его папой.


> ⚠️ Если у вас нет `preview.png` в папке `images`, просто удалите строку с `![Preview](images/preview.png)`.

Хотите, чтобы я добавил в README конкретные имена файлов из вашей папки `images` или пример `index.html`?
