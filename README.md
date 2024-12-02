# Laravel11 api és authentikáció, React login

## Laravel telepítése
<a href="https://www.youtube.com/watch?v=LmMJB3STuU4&list=PL38wFHH4qYZUXLba1gx1l5r_qqMoVZmKM">Videó alapján</a>

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

    APP_URL=http://localhost
    FRONTEND_URL=http://localhost:3000
    SANCTUM_STATEFUL_DOMAINS=localhost:3000

A SESSION_DRIVER értékét állítsuk át cookie-ra, hogy a fontend oldali kiszolgálónk tudja kezelni a csrf tokent
Valamint a SESSION_DOMAIN értékét localhostra kell állítani

    SESSION_DRIVER=cookie
    SESSION_DOMAIN=localhost

 Szintén a telepítés során a kérdésekre adott válaszokkal konfigurálható és az adatbázis rögtön migrálható is.
 Ne felejtsd el az api key-t generálni, ha nem tette volna meg a telepítő automatikusan!

    php artisan key:generate

## Felhasználó létrehozása és migrálása az adatbázisba: 

    php artisan migrate:fresh --seed

## React telepítése

Az alábbi <a href="https://www.youtube.com/watch?v=LPaSteXj0MQ&list=PL6tf8fRbavl2Y9nntlYBVS64bk28ffekB&index=2">videó</a> vite-tel telepíti, de a lényeg ugyanaz. 

    npx create-react-app react_frontend

## Alapcsomagok telepítése

1. <a href="https://react-bootstrap.netlify.app/docs/getting-started/introduction">react bootstrap</a>
        npm install react-bootstrap bootstrap

    Ne felejstd el az index.js-be importálni:

        import 'bootstrap/dist/css/bootstrap.min.css';

2. <a href="https://www.npmjs.com/package/axios">axios</a>
        npm install axios

3. <a href="https://reactrouter.com/home">react router </a>
        npm install react-router


Ne feledd, hogy a frontend és a backend alkalmazást külön VS Code ablakban indítsd el!



