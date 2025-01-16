# BimsCodes Ai Assisten

<p align="center">
  <img src="https://github.com/bimadevs/bimscodes-extenstion-documentation/blob/main/assets/using%20prompt.gif?raw=true" width="100%" />
</p>

BimsCodes adalah sebuah ai assisten yang dapat membantu kamu dalam coding

 <a style="background: red; padding: 6px 10px; color:white; border-radius: 4px" href="https://saweria.co/bimadev" class="cta-button">Dukung Saya di Saweria</a> 

Terima Kasih Kepada [Claude 3.5 Sonnet's agentic coding capabilities](https://www-cdn.anthropic.com/fed9cc193a14b84131812372d8d5857f8f304c52/Model_Card_Claude_3_Addendum.pdf) dan Cline sehingga saya dapat mengembangkan BimsCodes.

BimsCodes dapat menangani tugas pengembangan perangkat lunak yang kompleks selangkah demi selangkah. Dengan alat yang memungkinkannya membuat & mengedit berkas, menjelajahi proyek besar, menggunakan peramban, dan menjalankan perintah terminal (setelah Anda memberikan izin), dia bisa membantu Anda dengan cara-cara yang lebih dari sekadar penyelesaian kode atau dukungan teknis. BimsCodes bahkan dapat menggunakan Model Context Protocol (MCP) untuk membuat alat baru dan memperluas kemampuannya sendiri. Meskipun skrip AI otonom biasanya berjalan di lingkungan sandbox, ekstensi ini menyediakan GUI human-in-the-loop untuk menyetujui setiap perubahan file dan perintah terminal, sehingga menyediakan cara yang aman dan mudah diakses untuk mengeksplorasi potensi AI agen.


1. Masukkan tugas Anda dan tambahkan gambar untuk mengonversi maket menjadi aplikasi fungsional atau memperbaiki bug dengan tangkapan layar.
2. BimsCodes dimulai dengan menganalisis struktur file & AST kode sumber Anda, menjalankan pencarian regex, dan membaca file yang relevan untuk mempercepat proyek yang ada. Dengan mengelola informasi yang ditambahkan ke dalam konteks secara hati-hati, BimsCodes dapat memberikan bantuan yang berharga bahkan untuk proyek yang besar dan kompleks tanpa membebani jendela konteks.
3. Setelah BimsCodes memiliki informasi yang dibutuhkannya, dia bisa:
    - Membuat dan mengedit file + memonitor kesalahan linter/kompiler di sepanjang jalan, sehingga ia dapat secara proaktif memperbaiki masalah seperti impor yang hilang dan kesalahan sintaksis sendiri.
    - Menjalankan perintah secara langsung di terminal Anda dan memantau keluarannya saat dia bekerja, membiarkan dia misalnya, bereaksi terhadap masalah server dev setelah mengedit file.
    - Untuk tugas-tugas pengembangan web, BimsCodes dapat meluncurkan situs di peramban tanpa kepala, mengklik, mengetik, menggulir, dan menangkap tangkapan layar + log konsol, memungkinkannya untuk memperbaiki kesalahan waktu proses dan bug visual.
4. Ketika sebuah tugas selesai, BimsCodes akan menampilkan hasilnya kepada Anda dengan perintah terminal seperti `open -a “Google Chrome” index.html`, yang dapat Anda jalankan dengan satu klik tombol.

> [!TIP]
> Gunakan Shortcut `CMD/CTRL + Shift + P` untuk membuka palet perintah dan ketik “BimsCodes: Buka di Tab Baru” untuk membuka ekstensi sebagai tab di editor Anda. Hal ini memungkinkan Anda menggunakan BimsCodes berdampingan dengan file explorer Anda, dan melihat bagaimana ia mengubah ruang kerja Anda dengan lebih jelas.

---

<img align="right" width="340" src="https://github.com/user-attachments/assets/3cf21e04-7ce9-4d22-a7b9-ba2c595e88a4">

### Use any API and Model

BimsCodes mendukung penyedia API seperti OpenRouter, Anthropic, OpenAI, Google Gemini, AWS Bedrock, Azure, dan GCP Vertex. Anda juga dapat mengonfigurasi API yang kompatibel dengan OpenAI, atau menggunakan model lokal melalui LM Studio/Ollama. Jika Anda menggunakan OpenRouter, ekstensi ini mengambil daftar model terbaru mereka, memungkinkan Anda untuk menggunakan model terbaru segera setelah tersedia.

<p align="center">
  <img src="https://github.com/bimadevs/bimscodes-extenstion-documentation/blob/main/assets/use%20api.gif?raw=true" width="100%" />
</p>

Ekstensi ini juga melacak total token dan biaya penggunaan API untuk seluruh putaran tugas dan permintaan individual, sehingga Anda selalu mendapat informasi tentang pengeluaran di setiap perintah.



<!-- Transparent pixel to create line break after floating image -->

<img width="2000" height="0" src="https://github.com/user-attachments/assets/ee14e6f7-20b8-4391-9091-8e8e25561929"><br>

<img align="right" width="400" src="https://github.com/user-attachments/assets/c5977833-d9b8-491e-90f9-05f9cd38c588">

### Create and Edit Files

BimsCodes dapat membuat dan mengedit file secara langsung di editor Anda, menampilkan tampilan perbedaan dari perubahan. Anda bisa mengedit atau mengembalikan perubahan yang dilakukan BimsCodes secara langsung di editor diff view, atau memberikan umpan balik dalam chat sampai Anda puas dengan hasilnya. BimsCodes juga memonitor kesalahan linter/kompiler (impor yang hilang, kesalahan sintaksis, dll.) sehingga dia dapat memperbaiki masalah yang muncul di sepanjang jalan sendiri.

Semua perubahan yang dibuat oleh BimsCodes dicatat dalam Timeline file Anda, sehingga memudahkan untuk melacak dan mengembalikan modifikasi jika diperlukan.

<!-- Transparent pixel to create line break after floating image -->


### Use the Browser

Dengan Claude 3.5 Sonnet's terbaru [Computer Use](https://www.anthropic.com/news/3-5-models-and-computer-use) capability, BimsCodes dapat meluncurkan browser, mengeklik elemen, mengetik teks, dan scroll, menangkap tangkapan layar dan log konsol pada setiap langkah. Hal ini memungkinkan debugging interaktif, end-to-end testing, dan bahkan penggunaan web secara umum! Hal ini memberinya otonomi untuk memperbaiki bug visual dan masalah runtime tanpa Anda perlu memegang dan menyalin-tempel log kesalahan sendiri.

Coba minta BimsCodes untuk “test the app”, dan lihatlah bagaimana dia menjalankan perintah seperti `npm run dev`, meluncurkan server dev yang berjalan secara lokal di browser, dan melakukan serangkaian pengujian untuk mengonfirmasi bahwa semuanya berfungsi.


### Checkpoints: Compare and Restore

Saat BimsCodes mengerjakan sebuah tugas, ekstensi ini mengambil cuplikan ruang kerja Anda pada setiap langkah. Anda bisa menggunakan tombol 'Compare' untuk melihat perbedaan antara snapshot dan ruang kerja Anda saat ini, dan tombol 'Restore' untuk kembali ke titik tersebut.

Misalnya, saat bekerja dengan server web lokal, Anda dapat menggunakan 'Restore Workspace Only' untuk menguji berbagai versi aplikasi Anda dengan cepat, lalu gunakan 'Restore Task and Workspace' saat Anda menemukan versi yang ingin Anda lanjutkan. Dengan demikian, Anda dapat dengan aman menjelajahi berbagai pendekatan tanpa kehilangan progress anda.

## License

[Apache 2.0 © 2024 BimsCodes.](./LICENSE)
