# 💻 **Git Workflow ala Anak Gaul**  
Yo, bro/sis! Ini tutorial pake Git yang gampang dan asik buat nyimpen atau update project lo di GitHub. Langsung gas aja, ya!  

---

## 🎬 **Cara Upload Project Pertama Kali**  
1. Login ke GitHub, bikin repo baru (kasih nama sekeren mungkin).  
2. Di komputer/laptop lo:  
   - Arahkan terminal ke folder project lo:  
     ```bash  
     cd /var/www/html/aplikasi/  
     ```  
     *(Atau klik kanan folder -> Open in Terminal. Kalau pake VSCode, ketik `code .` terus buka terminal di situ).*  
   - Lanjutin pake perintah ini satu-satu:  
     ```bash  
     git init  
     git remote add origin (link-repo-lo)  
     git remote -v  
     git add .  
     git commit -m "Upload pertama, mantap!"  
     git push -u origin master  
     ```  
   - Kalau diminta, tinggal masukin username & password GitHub (atau token, kalo udah diatur).  

---

## 🔄 **Cara Upload Update (Perubahan Baru)**  
1. Pindah ke folder project lo:  
   ```bash  
   cd /var/www/html/aplikasi/  
   ```  
2. Cek file yang berubah:  
   ```bash  
   git status  
   ```  
3. Kalau mau upload perubahan:  
   - Cuma 1 file:  
     ```bash  
     git add namafile.php  
     ```  
   - Semua file (biar gak ribet):  
     ```bash  
     git add .  
     ```  
4. Commit perubahan:  
   ```bash  
   git commit -m "Update keren, bro!"  
   ```  
5. Push ke GitHub:  
   ```bash  
   git push origin master  
   ```  

---

## 🕵️ **Liat Log Perubahan (Histori)**  
Mau ngecek siapa ngapain kapan? Gas:  
```bash  
git log  
```  

---

## 🌱 **Bikin Branch Baru (Buat Fitur atau Cabang Baru)**  
1. Bikin branch baru (kek cabang, bro):  
   ```bash  
   git checkout -b namaBranchBaru  
   ```  
2. Cek daftar branch:  
   ```bash  
   git branch  
   ```  
3. Upload branch baru ke GitHub:  
   ```bash  
   git push --set-upstream origin namaBranchBaru  
   ```  
4. Di GitHub, bikin **Pull Request** dari branch baru ke `master`, terus **merge**.  
5. Kalau udah kelar, hapus branch-nya biar gak numpuk:  
   ```bash  
   git branch --delete namaBranchBaru  
   ```  
6. Balik lagi ke `master` dan tarik semua update:  
   ```bash  
   git checkout master  
   git pull  
   ```  

---

## 🚀 **Balik ke Commit Sebelumnya (Undo Salah Langkah)**  
1. Reset biasa:  
   ```bash  
   git reset kode_angka_commit  
   ```  
2. Reset total (biar bersih):  
   ```bash  
   git reset --hard  
   ```  

---

Segitu aja, gampang kan? Kalau masih bingung, inget: Googling adalah sahabat kita! ✌️
