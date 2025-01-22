# GitHub_Workflow
Ini adalah Perintah Git (indo_version)

## Perintah Dalam Git
### Upload project
Di web github, login dan Buat repository baru sesuai nama aplikasi
### Di komputer
 - cd /var/www/html/aplikasi/ (atau pilih folder (aplikasi) open in terminal, ketik (code .) buka terminal melalui vscode / (atau bisa juga lewat gitbash)
 - git init
 - git remote add origin (....link repository kalian.....)
 - git remote -v
 - git add .
 - git commit -m 'Upload pertama'
 - git push -u origin master
 - Masukkan username dan password github (jika ada)

### Upload pembaharuan
* cd /var/www/html/aplikasi/
* git status // bakal ditampilkan daftar file yg mengalami perubahan
* git add namafile.php // update 1 file ke server
* git commit // update semua file ke server
* git push origin master // masukkan username dan password
* git log // cek perubahan di log

### Baca perubahan
- cd /var/www/html/aplikasi/
- git log

### Buat cabang aplikasi (Branch Baru)
* git checkout -b cabangAplikasi
* git branch // lihat daftar cabang repo
* git push --set-upstream origin cabangAplikasi // usulkan pull request ke master
* Buka web github/repo terima confirm pull request dan merge ke master
* Delete branch yg sudah disetujui kalau tidak diperlukan lagi
* git checkout master // kembali ke repo master
* git pull // tarik semua pembaharuan dari server
* git branch --delete cabangAplikasi

### Kembali ke commit sebelumnya
- git reset kode_angka_commit
- git reset --hard
