# praktikum-git-556473
SS buktirestriction:

![Bukti Protection Rule](BuktiRestriction.png)
Commit:
* 6ac7ad0 (HEAD -> main, origin/main, origin/HEAD) style:new_style+gitignore
* 654921f feat:new
* f6ac1c4 Commit Pertama
* f1c455b Commit Pertama
* 5b26e3a Initial commit

 Laporan Praktikum Git & GitHub

**Nama:** Aulia Muttaqin Lubis  
**Program Studi:** Teknologi Rekayasa Perangkat Lunak  
**Universitas:** Universitas Gadjah Mada  


 Deskripsi Proyek
Proyek ini merupakan bagian dari tugas praktikum untuk mengimplementasikan alur kerja Git yang standar dalam pengembangan perangkat lunak. Fokus utama dari praktikum ini adalah penguasaan perintah dasar Git, manajemen cabang (*branching*), penanganan konflik (*merge conflict*), penggunaan fitur-fitur GitHub seperti *Pull Request* dan *Issue Tracking*, serta penerapan *Branch Protection Rules*.

---

  Tugas 1: Inisialisasi & Riwayat Commit

Pada tahap awal, repository diinisialisasi dan dihubungkan ke GitHub. Dilakukan beberapa commit awal menggunakan standar **Conventional Commits** (seperti `feat:`, `style:`, `fix:`) untuk memastikan riwayat perubahan yang rapi dan informatif. Selain itu, file `.gitignore` ditambahkan untuk memastikan file sampah (seperti `.DS_Store` atau `node_modules/`) tidak ikut terunggah.

**Log Riwayat Git:**
Perintah `git log --oneline --graph` digunakan untuk memantau struktur commit dan percabangan secara visual di terminal.
![New Branch create](New%20Branch%20create.png)

---

 Tugas 2: Branching & Pull Request

Pengembangan fitur dilakukan di cabang terpisah dari `main` untuk menjaga stabilitas kode utama. Cabang yang dibuat antara lain `feature/navbar`, `feature/footer`, dan `hotfix/typo`.

 Alur Kerja Branching:
1. **Push Branch:** Mengunggah branch lokal ke remote repository.
   ![Branch push](Branch%20push.png)
2. **Membuat Pull Request (PR):** Mengajukan penggabungan kode dari branch fitur ke branch utama.
   ![Create Pull req](Create%20Pull%20req.png)
3. **Merging:** Penggabungan dilakukan setelah kode dipastikan aman. Untuk fitur digunakan metode *Squash and merge*.
   ![Merge pull](Merge%20pull.png)

 Branch Protection Rules
Untuk mencegah kesalahan fatal (seperti *direct push* ke `main`), aturan perlindungan branch diterapkan. Aturan ini mewajibkan adanya *Pull Request* dan persetujuan minimal satu orang sebelum penggabungan.
![Screenshot 2026-05-01 005143](Screenshot%202026-05-01%20005143.png)

*Dalam kondisi tertentu, admin dapat melakukan bypass aturan ini untuk pembaruan cepat (Restriction Update).*
![restriction update](restriction%20update.png)

---

 Tugas 3: Manajemen Konflik & Rebase

Konflik disimulasikan dengan mengubah variabel warna background yang sama di dua branch berbeda (`experiment/color-A` dan `experiment/color-B`). 

 Resolusi Konflik:
- **Secara Lokal:** Konflik dideteksi dan diselesaikan secara manual di VS Code dengan memilih perubahan mana yang akan dipertahankan.
  ![Konflik bgcolor](Konflik%20bgcolor.png)
- **Melalui GitHub:** Setelah konflik di-resolve secara lokal, penggabungan dapat dikonfirmasi melalui antarmuka web GitHub.
  ![commit merge](commit%20merge.png)

---

 Tugas 4: Dokumentasi & Issue Tracking

Manajemen tugas dan bug dilakukan menggunakan fitur **GitHub Issues**. Setiap tugas dikaitkan dengan nomor issue tertentu agar progres terdokumentasi dengan baik.

 Issue Tracking & Closing:
1. **Membuat Issue:** Mendefinisikan fitur baru atau bug yang ditemukan.
   ![Issue Create](Issue%20Create.png)
2. **Otomatisasi Penutupan Issue:** Menggunakan kata kunci (seperti `Closes #nomor_issue`) di deskripsi PR agar issue tertutup secara otomatis saat PR di-merge.
   ![Closing Issue](Closing%20Issue.png)




 Referensi Perintah Git yang Digunakan

| Perintah | Deskripsi |
| :--- | :--- |
| `git init` | Menginisialisasi repositori Git baru. |
| `git commit -m "pesan"` | Menyimpan perubahan ke riwayat repositori. |
| `git push -u origin [nama_branch]` | Mengunggah branch lokal ke GitHub. |
| `git log --oneline --graph` | Melihat visualisasi riwayat commit. |
| `git rebase -i` | Melakukan pembersihan atau penggabungan commit (*squash*). |
| `git switch -c [nama_branch]` | Membuat branch baru dan langsung berpindah ke dalamnya. |