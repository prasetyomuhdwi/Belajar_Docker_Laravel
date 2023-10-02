# 2 Oct 2023
## Project laravel 9 with docker compose:
| image | version |
| ----------- | ----------- |
|nginx|stable-alpine|
|mysql|8.0.30|
|php|8.2-fpm-alpine|
|composer|2.5.5|
|npm node|16.15.0|
|artisan| |
|||

## 🤠 Cara Kerja
- ### Docker-compose build nginx, mysql, and php:

```Shell
docker-compose up -d --build
```

- ### Tambahkan file .env, cari file di folder "src"

```Shell
cd src
```
- #### Copy file .env.example lalu ubah jadi .env

```Shell
cp .env.example .env
```

- ### Update folder /vendor dan Auto load

```Shell
docker-compose run --rm composer update
```

- ### Generate Key app laravel

```Shell
docker-compose run --rm artisan key: generate
```

- ### Jalankan proyek di browser lokal

```Shell
localhost:8080
```
- ### Jalankan perintah laravel + docker

```Shell
docker-compose run --rm <"perintah laravel, contohnya migrate">
```
atau

```Shell
docker-compose run --rm install <"package, contoh untuk npm">
```

## 🤓 Project ini akan sedikit memberikan gambaran mengenai:
- Cara membuat docker compose yang sesuai untuk pengembangan web laravel, seperti:
    - melakuakan pengaturan pada docker-compose.yml
    - melakuakan pengaturan pada Dockerfile
    - serta melakuakan pengaturan pada nginx
- Cara menghubungkan project laravel ke docker:
    - melakukan koneksi ke database mysql di docker
    - menginstall package node.js

