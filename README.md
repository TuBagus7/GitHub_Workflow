# 💻 **Git Workflow ala Tu Bagus **  
Ini tutorial pake Git yang gampang dan asik buat nyimpen atau update project kalian di GitHub. Langsung gas aja, ya!  

---

## 🎬 **Cara Upload Project Pertama Kali**  
1. Login ke GitHub, bikin repo baru (kasih nama sesuai apa aplikasi yang kamu buat atau kasih nama sekeren mungkin).  
2. Di komputer/laptop kalian:  
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

## 🎯 **Sinkronisasi dengan Repo di GitHub (Pull Update dari Remote Repo)**  
- Kalau mau update project di lokal dengan perubahan terbaru dari GitHub:  
  ```bash  
  git pull origin master  
  ```  

---

## 🤔 **Hapus File dari Repo (Git Remove)**  
- Kalau mau hapus file dari repository (tapi tetep simpan di lokal):  
  ```bash  
  git rm --cached namafile  
  ```  
- Kalau mau hapus file dari repository dan lokal sekaligus:  
  ```bash  
  git rm namafile  
  ```  

---

## 🔍 **Liat Bedanya (Diff)**  
- Buat cek perbedaan antara file yang diubah dengan yang di-commit:  
  ```bash  
  git diff  
  ```  

---

## 📂 **Cloning Repository**  
- Kalau mau ambil repo dari GitHub (buat pertama kali):  
  ```bash  
  git clone link-repo  
  ```  

---

## 🚮 **Hapus Branch**  
- Kalau mau hapus branch di lokal (karena udah gak dipakai):  
  ```bash  
  git branch -d namaBranch  
  ```  
- Kalau branch udah dihapus di remote:  
  ```bash  
  git push origin --delete namaBranch  
  ```  

---

## 🔧 **Merge Branch**  
- Kalau mau gabung branch tertentu ke `master` (di lokal):  
  ```bash  
  git checkout master  
  git merge namaBranch  
  ```  

---

## 🔒 **Amankan Commit Terakhir (Amend)**  
- Kalau mau edit commit terakhir (misal: salah pesan commit):  
  ```bash  
  git commit --amend -m "Pesan baru"  
  ```  

---

## 🧹 **Bersihin File Tak Terpakai (Clean)**  
- Kalau mau hapus file yang gak di-track (belum di-add):  
  ```bash  
  git clean -f  
  ```  

---

## 🔙 **Restore Code dari Github**
- Apa bila di lokal kalian, ada file yang tidak sengaja terhapus, tapi di git repo masih ada, bisa di restore
```bash  
 git restore --source=main (folder atau file yang hilang)  
  ```  
Segitu aja, gampang kan? Kalau masih bingung, inget: Stackoverflow adalah sahabat kita!, atau GPT eiiits... ✌️
