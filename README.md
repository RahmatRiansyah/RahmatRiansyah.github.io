Maaf, Website Sedang Mengalami Gangguan

Kami mohon maaf atas ketidaknyamanan ini. Saat ini, website sedang mengalami gangguan teknis. Silakan lakukan salah satu dari langkah berikut:

- Refresh halaman Anda untuk mencoba kembali.
- Kunjungi kembali website beberapa saat lagi.

Tim kami sedang bekerja untuk memperbaiki masalah ini secepat mungkin. Terima kasih atas pengertian dan kesabaran Anda.

# Personal Blog dengan Hugo

Selamat datang di repository Personal Blog yang dibangun menggunakan Hugo! Proyek ini merupakan bagian dari UAS untuk mata kuliah Pengantar Rekayasa Perangkat Lunak.

## Langkah Instalasi dan Konfigurasi Proyek

Berikut adalah langkah-langkah untuk menginstal dan mengkonfigurasi proyek ini:

### Prerequisites

Sebelum memulai, pastikan Anda memiliki hal-hal berikut:

- [Hugo](https://gohugo.io/getting-started/quick-start/) (versi terbaru)
- [Git](https://git-scm.com/) (versi terbaru)
- Text editor (seperti Visual Studio Code, Sublime Text, atau Atom)

### Langkah Instalasi

1. **Clone repository ini:**

   ```bash
   git clone https://github.com/RahmatRiansyah/RahmatRiansyah.github.io.git
   ```

2. **Masuk ke direktori proyek:**

   ```bash
   cd RahmatRiansyah.github.io
   ```

3. **Instal Hugo:**
   - Ikuti petunjuk di [sini](https://gohugo.io/getting-started/quick-start/) untuk menginstal Hugo sesuai dengan sistem operasi Anda.

4. **Jalankan situs secara lokal:**

   ```bash
   hugo server
   ```

   Akses situs Anda di [http://localhost:1313](http://localhost:1313).

### Konfigurasi

1. **Edit file `config/_default/hugo.yaml`:**
   - Sesuaikan pengaturan berikut:
     ```yaml
     title: "Portofolio Rahmat Riansyah"
     baseURL: "https://portofoliorahmatriansyah.github.io/"
     ```

2. **Edit file `config/_default/params.yaml`:**
   - Sesuaikan pengaturan berikut:
     ```yaml
     appearance:
       mode: "system"
       color: "emerald"
     marketing:
       seo:
         site_type: "Person"
         description: "The highly-customizable Hugo Academic theme powered by Hugo Blox Builder."
     ```

3. **Edit file `config/_default/menus.yaml`:**
   - Tambahkan menu navigasi:
     ```yaml
     main:
       - name: "Bio"
         url: "/"
         weight: 10
       - name: "Papers"
         url: "/#papers"
         weight: 11
       - name: "News"
         url: "/#news"
         weight: 13
       - name: "Experience"
         url: "/experience/"
         weight: 20
       - name: "Projects"
         url: "/projects/"
         weight: 30
     ```

4. **Edit file `content/_index.md`:**
   - Sesuaikan konten halaman utama:
     ```md
     ---
     title: ""
     date: 2024-12-26T08:08:08Z
     type: landing
     design:
       spacing: "6rem"
     sections:
       - block: resume-biography-3
         content:
           username: Admin
           text: ""
           button:
             text: Download CV
             url: https://drive.google.com/file/d/13T5Fzm80i1R3KQFEXD-b04DGRXy3Q-TP/view?usp=drive_link
         design:
           css_class: dark
           background:
             color: black
             image:
               filename: stacked-peaks.svg
               filters:
                 brightness: 1.0
               size: cover
               position: center
               parallax: false
       - block: markdown
         content:
           title: "📚 My Research"
           subtitle: "Exploring Software Engineering Innovations"
           text: |-
             As a Software Engineering student, I am particularly interested in the following areas:
             - **Machine Learning**
             I am always looking for opportunities to collaborate on exciting projects and research. Please feel free to reach out if you are interested in working together! 😃
         design:
           columns: "1"
       - block: collection
         id: papers
         content:
           title: Featured Publications
           filters:
             folders:
               - publication
             featured_only: true
         design:
           view: article-grid
           columns: 2
       - block: collection
         content:
           title: Recent Publications
           text: ""
           filters:
             folders:
               - publication
             exclude_featured: false
         design:
           view: citation
       - block: collection
         id: news
         content:
           title: Recent News
           subtitle: ""
           text: ""
           page_type: post
           count: 5
           filters:
             author: ""
             category: ""
             tag: ""
             exclude_featured: false
             exclude_future: false
             exclude_past: false
             publication_type: ""
           offset: 0
           order: desc
         design:
           view: date-title-summary
           spacing:
             padding: [0, 0, 0, 0]
     ```

5. **Edit file `content/authors/admin/_index.md`:**
   - Sesuaikan profil singkat:
     ```md
     ---
     title: "Rahmat Riansyah"
     first_name: Rahmat
     last_name: Riansyah
     role: Software Engineering Student
     organizations:
       - name: Institut Teknologi Statistika dan Bisnis Muhammadiyah Semarang
         url: https://itesa.ac.id/
     profiles:
       - icon: at-symbol
         url: mailto:rahmatriansyahpkp@gmail.com
         label: E-mail Me
     interests:
       - Artificial Intelligence
     education:
       - area: S1 Software Engineering
         institution: Institut Teknologi Statistika dan Bisnis Muhammadiyah Semarang
         date_start: 2023-10-07T08:08:08Z
         date_end: ""
         summary: |
           Relevant courses: Learning the systematic processes associated with project design, programming languages, development, testing, maintenance, and software management.
     work:
       - position: Daily Worker
         company_name: PT Shopee Express
         date_start: 2024-02-03
         date_end: ""
         summary: |
           • Responsible for the sorting and organizing of goods to ensure delivery efficiency.
     skills:
       - name: Technical Skills
         items:
           - name: Python
             percent: 80
       - name: Hobbies
         items:
           - name: FootBall
             percent: 100
     languages:
       - name: English
         percent: 30
     awards:
       - title: Career Essentials in Generative AI by Microsoft and LinkedIn
         url: https://drive.google.com/file/d/1EEeoRLPXhAlBGrZxcz90s58ioHE6c1y0/view?usp=sharing
         date: "2024-05-16"
         awarder: Microsoft

     ```

Pastikan untuk menyesuaikan bagian lain sesuai dengan kebutuhan dan informasi spesifik proyek Anda.
        

### Memastikan Perubahan Tercermin

Setelah Anda melakukan semua perubahan di atas, jalankan server Hugo Anda dengan perintah berikut untuk melihat perubahan:
```bash
hugo server
### Memastikan Perubahan Tercermin

Setelah Anda melakukan semua perubahan di atas, jalankan server Hugo Anda dengan perintah berikut untuk melihat perubahan:
```bash
hugo server
```
Kemudian buka browser dan akses `http://localhost:1313` untuk melihat tampilan blog Anda.


### Publikasi

1. **Host blog secara gratis:**
   - Untuk menghosting blog Anda, Anda bisa menggunakan GitHub Pages. Ikuti langkah-langkah berikut:
     - Buat branch `gh-pages` di repository Anda.
     - Jalankan perintah berikut untuk membangun situs dan menyalin hasilnya ke branch `gh-pages`:
       ```bash
       hugo
        cd public
        git init
        git remote add origin https://github.com/RahmatRiansyah/RahmatRiansyah.github.io.git
        git checkout -b gh-pages
        git add .
        git commit -m "Deploy to GitHub Pages"
        git push origin gh-pages --force
       ```

## Tautan ke Situs Blog

Blog Anda dapat diakses di [https://rahmatriansyah.github.io/](https://rahmatriansyah.github.io/).

## Lisensi

Proyek ini dilisensikan di bawah [MIT License](LICENSE).
```

### Catatan:

- Gantilah "username" dengan nama pengguna GitHub Anda dan `nama-tema-yang-dipilih` dengan nama tema yang Anda gunakan.
- Pastikan untuk menyesuaikan bagian lain sesuai dengan kebutuhan dan informasi spesifik proyek Anda.
- Pastikan Anda menyimpan semua perubahan yang telah Anda buat.
- Jika Anda tidak menemukan file tertentu, periksa dokumentasi tema Academic CV untuk informasi lebih lanjut tentang struktur file dan cara menyesuaikan tema.
- Anda juga dapat menambahkan lebih banyak informasi di file `config/_default/params.yaml` untuk menyesuaikan lebih lanjut tampilan dan fungsi blog Anda.