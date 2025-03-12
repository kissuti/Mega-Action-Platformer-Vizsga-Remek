# 🌐 **Mega Action Platformer - Weboldal + Launcher**  
[![PHP](https://img.shields.io/badge/PHP-%5E8.0-blue)](https://www.php.net/)  
[![CSS](https://img.shields.io/badge/CSS-SASS%2FSCSS-ff69b4)](https://sass-lang.com/)  

Üdvözöllek a **Mega Action Platformer** projektben! 🎉 Ez a projekt egy teljes értékű weboldal, amely tartalmaz regisztrációs és bejelentkezési rendszert, adminisztrációs panelt, valamint egy játékindító (launcher) rendszert automatikus frissítésekkel. 🚀  

---

## 🚀 Aktív Kollaborátorok
| 👤 **Név**        | 🔗 **GitHub Profil** | 
|-------------------|-----------------------|
| 🧑‍💻 Rómeó | [GitHub Profil](https://github.com/KalmanRomeo) |
| 🧑‍💻 Szabi | [GitHub Profil](https://github.com/Szabi0147) |
| 🧑‍💻 Milán | [GitHub Profil](https://github.com/DagobertBacsi) |

---

## 🛠 **Technológiák**  

### Backend  
- **PHP 8.0+**: Erőteljes és gyors szerveroldali nyelv.  
- **MySQL**: Adataid biztonságos tárolása egy strukturált adatbázisban.  

### Frontend  
- **HTML5**: A modern és reszponzív weboldal alapja.  
- **CSS (SASS)**: Stílusos és könnyen karbantartható megjelenés.  
- **JavaScript**: Interaktív elemek és dinamikus funkciók.  

### Extra funkciók  
- **Admin Panel**: Kezeld az érméket és felhasználókat egyszerűen.  
- **Launcher**: A játékindító automatikus frissítési funkcióval.

![C#](https://img.shields.io/badge/c%23-%23239120.svg?style=for-the-badge&logo=csharp&logoColor=white) ![CSS3](https://img.shields.io/badge/css3-%231572B6.svg?style=for-the-badge&logo=css3&logoColor=white) ![HTML5](https://img.shields.io/badge/html5-%23E34F26.svg?style=for-the-badge&logo=html5&logoColor=white)  ![.Net](https://img.shields.io/badge/.NET-5C2D91?style=for-the-badge&logo=.net&logoColor=white) ![SASS](https://img.shields.io/badge/SASS-hotpink.svg?style=for-the-badge&logo=SASS&logoColor=white) ![MicrosoftSQLServer](https://img.shields.io/badge/Microsoft%20SQL%20Server-CC2927?style=for-the-badge&logo=microsoft%20sql%20server&logoColor=white)

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/tobiasmeyhoefer/tobiasmeyhoefer/output/github-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/tobiasmeyhoefer/tobiasmeyhoefer/output/github-snake.svg" />
  <img alt="github-snake" src="https://raw.githubusercontent.com/tobiasmeyhoefer/tobiasmeyhoefer/output/github-snake.svg" />
</picture>

---

## 📂 **Projektstruktúra**  

```plaintext
MAP Website/
├── images/               # Képek tárolása
├── assets/               # Statikus fájlok
│   ├── css/              # Stíluslapok
│   ├── js/               # JavaScript fájlok
│   ├── sass/             # SASS forráskódok
│   └── webfont/          # Webes betűkészletek
├── php/                  # PHP fájlok
│   ├── scoreboard.php    # Scoreboard funkció
│   ├── register.php      # Regisztráció logika
│   ├── login.php         # Bejelentkezés logika
│   ├── admin.php         # Admin panel
│   ├── register.css      # Regisztráció stíluslap
│   ├── login.css         # Bejelentkezés stíluslap
│   ├── admin.css         # Admin panel stíluslap
│   └── scoreboard.css    # Scoreboard stíluslap
├── index.html            # Kezdőlap
└── README.md             # Dokumentáció
```

## 📋 **Telepítés**  

### 1️⃣ Előfeltételek  

#### Weboldalhoz  
- **XAMPP**: PHP, MySQL és Apache webszerver egyszerűen telepíthető környezetben. [Töltsd le itt](https://www.apachefriends.org/index.html).  
- Egy programozó szoftver, például **Visual Studio Code** vagy **PhpStorm**.  

#### Launcherhez  
- **.NET Core 3.1**: A játékindító fejlesztéséhez szükséges keretrendszer. [Töltsd le itt](https://dotnet.microsoft.com/download/dotnet/3.1).  
- A **Visual Studio 2019+** programozó szoftver.  

---

### 2️⃣ Weboldal telepítése  

1. **XAMPP beállítása**:  
   - Telepítsd a XAMPP-ot, és indítsd el az Apache és MySQL modulokat.  
2. **Projekt másolása**:  
   - Másold a `MAP Website` mappát a XAMPP `htdocs` könyvtárába (pl. `C:/xampp/htdocs/MAP Website/`).  
3. **Adatbázis importálása**:  
   - Nyisd meg a böngésződben a `http://localhost/phpmyadmin` oldalt.  
   - Hozz létre egy új adatbázist (`db_mega`), vagy másold ki a kódot lejjebb.  
4. **Weboldal elérése**:  
   - Lépj a böngésződben a `http://localhost/MAP Website/index.html` címre.

---
     
### 3️⃣ Launcher telepítése

1. **.NET Core környezet beállítása**:  
   - Telepítsd a .NET Core 3.1 runtime-ot és SDK-t.    
2. **Projekt megnyitása**:  
   - Nyisd meg a `GameLauncher.sln` fájlt.  
3. **Launcher futtatása**:  
   - Indítsd el a programot és az autómatikusan letölti neked a játékot.

### 🗄 **Adatbázis létrehozása**  

Használj MySQL-t vagy phpMyAdmin-t az alábbi SQL script futtatásához:  

```sql
-- Adatbázis létrehozása
CREATE DATABASE IF NOT EXISTS db_mega;

-- Adatbázis használata
USE db_mega;

-- Tábla létrehozása
CREATE TABLE IF NOT EXISTS users (
    id INT AUTO_INCREMENT PRIMARY KEY,      -- Egyedi azonosító, automatikusan növekvő
    username VARCHAR(50) NOT NULL,          -- Felhasználónév, maximum 50 karakter
    pass VARCHAR(255) NOT NULL,             -- Jelszó, titkosítva tárolva
    coin INT DEFAULT 0,                     -- Felhasználóhoz tartozó "coin", alapértelmezetten 0
    email VARCHAR(100) UNIQUE NOT NULL      -- E-mail cím, maximum 100 karakter, egyedi érték
);

CREATE TABLE IF NOT EXISTS transactions (
  id int(11) NOT NULL AUTO_INCREMENT,
  item_number varchar(50) DEFAULT NULL,
  item_name varchar(255) DEFAULT NULL,
  item_price float(10,2) DEFAULT NULL,
  item_price_currency varchar(10) DEFAULT NULL,
  payer_id varchar(50) DEFAULT NULL,
  payer_name varchar(50) DEFAULT NULL,
  payer_email varchar(50) DEFAULT NULL,
  payer_country varchar(20) DEFAULT NULL,
  merchant_id varchar(255) DEFAULT NULL,
  merchant_email varchar(50) DEFAULT NULL,
  order_id varchar(50) NOT NULL,
  transaction_id varchar(50) NOT NULL,
  paid_amount float(10,2) NOT NULL,
  paid_amount_currency varchar(10) NOT NULL,
  payment_source varchar(50) DEFAULT NULL,
  payment_status varchar(25) NOT NULL,
  created datetime NOT NULL,
  modified datetime NOT NULL,
  PRIMARY KEY (id)
) ENGINE=InnoDB DEFAULT CHARSET=utf8 COLLATE=utf8_unicode_ci;CREATE TABLE transactions (

CREATE TABLE IF NOT EXISTS licensz (
  id int(11) AUTO_INCREMENT NOT NULL PRIMARY KEY,
  payer_id varchar(50) NOT NULL,
  order_id varchar(50) NOT NULL,
  license_key varchar(24) NOT NULL,
  created_at timestamp NOT NULL DEFAULT current_timestamp(),
   banned BOOLEAN DEFAULT 0 
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_general_ci;

```

---

### 📸 **Képernyőképek**  

| **Weboldal**         | **Admin Panel**      | **Launcher**         |
|-----------------------|----------------------|----------------------|
| ![Weboldal Screenshot](MAP%20Website/images/screenshots/webpage.png) | ![Admin Panel Screenshot](MAP%20Website/images/screenshots/admin-panel.png) | ![Launcher Screenshot](MAP%20Website/images/screenshots/launcher.png) |

---

## 🚀 **Főbb funkciók**  

### 🌟 **Felhasználói modulok**  
- **Regisztráció**: Gyors és biztonságos.  
- **Bejelentkezés**: Gyors és biztonságos bejelentkezés.
- **Licensz Vásárlás**: Gyors és biztonságos vásárlás rendszer PayPal Api Használatával

### 🔒 **Admin Panel**  
- **Felhasználókezelés**: Felhasználók listázása, törlése, érmék módosítása, Licensz Tiltása (Banolása).    

### 📊 **Scoreboard**  
- **Élő eredménytábla**: Játékosok és érmék megjelenítése.  aaaaa
