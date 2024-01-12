## Запуск:

1. ```pip install -r requirements.txt```
2. Cоздать конфигурационный файл по пути - .config/cloudphoto/cloudphotorc

Формат конфигурационного файла (ini-файл):
```
bucket = INPUT_BUCKET_NAME 
aws_access_key_id = INPUT_AWS_ACCESS_KEY_ID 
aws_secret_access_key = INPUT_AWS_SECRET_ACCESS_KEY 
region = ru-central1 
endpoint_url = https://storage.yandexcloud.net 
```
3. Перед началом использования ввести команду:
```bash
python cloudphoto.py init
```

### Загрузка фотографий

Для отправки фотографий в облачное хранилище используйте команду `upload`:

```bash
python cloudphoto.py upload --album ALBUM_NAME [--path PHOTOS_DIR]
```

### Скачивание фотографий

Для загрузки фотографий из облачного хранилища используйте команду `download`:

```bash
python cloudphoto.py download --album ALBUM_NAME [--path PHOTOS_DIR]
```

### Просмотр списка альбомов

Для просмотра списка альбомов в облачном хранилище используйте команду `list`:

```bash
python cloudphoto.py list [--album ALBUM_NAME]
```

### Удаление альбомов и фотографий

Для удаления альбомов и фотографий используйте команду `delete`:

```bash
python cloudphoto.py delete --album ALBUM_NAME [--photo PHOTO_NAME]
```

### Создание веб-сайта

Для формирования и публикации веб-страниц фотоархива используйте команду `mksite`:

```bash
python cloudphoto.py mksite
```