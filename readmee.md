## Latihan: Membuat User dan Database pada PostgreSQL

1. Untuk memastikan konfigurasi berhasil, silakan buka Powershell/CMD kemudian tuliskan perintah.

```bash
psql --username developer --dbname companydb
```

2. Untuk membuat user
```bash
psql --username postgres
```
Membuat User Baru
```bash
CREATE USER <<nama user>> WITH ENCRYPTED PASSWORD '<<password>>';
```

contoh
```bash
CREATE USER developer WITH ENCRYPTED PASSWORD 'supersecretpassword';
```
3. Membuat Database
```bash
CREATE DATABASE <<nama database>>;
```

contoh
```bash
CREATE DATABASE companydb;
```

4. Memberikan Hak Akses Database ke User
```bash
GRANT ALL ON DATABASE <<nama database>> TO <<nama user>>;
ALTER DATABASE <<nama database>> OWNER TO <<nama user>>;
```

contoh
```bash
GRANT ALL ON DATABASE companydb TO developer;
ALTER DATABASE companydb OWNER TO developer;
```

5. Mengakses Database
Keluar terlebih dahulu
```bash
\q
```
Kemudian masuk lagi melalui psql
```bash
psql --username developer --dbname companydb
```
Kalau sudah muncul kode di bawah berari sudah berhasil
```bash
psql (17.4)
WARNING: Console code page (437) differs from Windows code page (1252)
         8-bit characters might not work correctly. See psql reference
         page "Notes for Windows users" for details.
Type "help" for help.
```

