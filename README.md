﻿   ```
   Source venv/bin/activate
   pip install -r requirements.txt
   python manage.py makemigrations
   python manage.py migrate
   python manage.py collectstatic
   python manage.py test 
   python manage.py createsuperuser
   python manage.py runserver
	
	views.py — это сердце веб-приложения, принимающего HTTP-запросы от веб-клиентов и возвращающего HTTP-ответы. Между этим они используют другие ресурсы фреймворка для доступа к базам данных, шаблонам визуализации и т. д.

	Models.py - определяет структуру хранимых данных, включая типы полей и, возможно, их максимальный размер, значения по умолчанию, параметры списка выбора, текст справки для документации, текст меток для форм и т. д.

	.html - Системы шаблонов позволяют указать структуру выходного документа, используя заполнители для данных, которые будут вставлены при генерировании страницы.

	Чтобы создать проект нам необходимо прописать django-admin startproject <Название проекта>

	settings.py содержит в себе все настройки проекта. Здесь мы регистрируем приложения, задаём размещение статичных файлов, настройки базы данных и так далее. 
	urls.py задаёт ассоциации url адресов с представлениями. Несмотря на то, что этот файл может содержать все настройки url, обычно его делят на части, по одной на приложение, как будет показано далее.
 
	wsgi.py используется для налаживания связи между вашим Django приложением и веб-сервером. Вы можете воспринимать его, как утилиту.
	
	Чтобы создать приложение необходимо прописать python manage.py startapp <Название приложения>

	Папка migrations используется, чтобы хранить "миграции" — файлы, которые позволяют вам автоматически обновлять базу данных по мере изменения моделей. 

	__init__.py — пустой файл для того, чтобы Django и Python распознавали папку как Python модуль и позволяет нам использовать его объекты внутри других частей проекта.

	Чтобы запустить приложение нам необходимо написать python manage.py runserver
	
	Для того чтобы создать суперпользователя мы пишем python manage.py createsuperuser.

	Для входа в админ-панель откройте ссылку /admin (например http://127.0.0.1:8000/admin)
