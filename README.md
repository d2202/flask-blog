# flask-blog

Небольшой проект блога чтобы потренироваться с основными фишками Flask

# Features:
- В качестве БД используется SQLite (+ Flask-SQLAlchemy)
- На фронтенде Flask-Bootstrap
- Для создания и отрисовки форм в шаблонах - Flask-WTForms
- Возможность регистрировать новых пользователей и логиниться от созданного пользователя
- Пароли пользователей хранятся в БД в зашифрованном виде (sha-256 + salt)
- Админ (пользователь с id = 1, по сути, первый созданный пользователь) может создавать, редактировать и удалять посты, остальные пользователи могут их просматривать и комментировать, это достигнуто с помощью:
  1) Flask Login, loginmanager в частности, разделяет пользователей и защищает страницы редактирования, добавления и удаления постов от неавторизированного пользователя без админских прав
  2) Возможность комментирования дополнена кастомным редактором CKEditor, в котором больше возможностей для форматирования текста
- Маленькая милая фича: генерация Gravatar для каждого пользователя на основе их email-хэшей (модуль flask-gravatar), чтобы комментарии не выглядели уныло.
