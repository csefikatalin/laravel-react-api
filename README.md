# Laravel11 api és authentikáció, React login

## Laravel telepítése

<a href="https://laravel.com/docs/11.x/installation">telepítési útmutató</a>

    laravel new example-app

A telepítés során válaszd a breeze-t és az api végpontokat. 

### .ENV fájl

Az env fájlban az alábbi változtatások kellenek.

    DB_CONNECTION=mysql
    DB_HOST=127.0.0.1
    DB_PORT=3306
    DB_DATABASE=laravel_react_api
    DB_USERNAME=root
    DB_PASSWORD=

    APP_URL=http://localhost:8000
    FRONTEND_URL=http://localhost:3000

 Szintén a telepítés során a kérdésekre adott válaszokkal konfigurálható és az adatbázis rögtön migrálható is. 

