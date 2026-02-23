SDM bertindak sebagai "pintu gerbang utama" (filter) yang mengatur lalu lintas keluhan. Ini sangat menguntungkan karena pegawai yang melapor tidak perlu pusing memikirkan "ini urusan divisi mana ya?". Mereka cukup lapor ke satu tempat, dan SDM yang mengatur sisanya.

Berikut adalah rincian alur sistem (Workflow) yang akan terjadi di aplikasi ANCHOR buatanmu nanti:

1. Fase Pelaporan (Oleh Pegawai)
Pegawai dari divisi manapun membuka portal, membuat tiket baru, dan mendeskripsikan masalahnya (misal: "Komputer nyala tapi layar gelap" atau "Kran air di toilet lantai 2 bocor"). Tiket otomatis berstatus "Menunggu Verifikasi SDM".

2. Fase Verifikasi & Distribusi (Oleh Admin SDM)
Akun dengan hak akses SDM membuka dashboard mereka. Mereka akan melihat semua tiket yang masuk.

SDM membaca keluhan.

SDM memilih unit yang bertanggung jawab (Misal: klik dropdown lalu pilih "Divisi IT" atau "Divisi Umum/Fasilitas").

Setelah di-assign, status tiket berubah menjadi "Diteruskan ke Unit".

3. Fase Eksekusi (Oleh Unit Terkait)
Akun dari Divisi IT atau Bagian Umum akan mendapat notifikasi atau melihat tiket masuk di dashboard khusus divisi mereka.

Teknisi mengambil tiket tersebut dan status berubah menjadi "Sedang Dikerjakan".

Setelah selesai diperbaiki, teknisi mengubah status menjadi "Selesai" dan bisa menambahkan catatan perbaikan (misal: "Kabel VGA sudah diganti baru").

4. Fase Laporan (Monitoring)
Karena SDM berada di hierarki tertinggi, mereka memiliki akses untuk melihat laporan keseluruhan. SDM bisa memantau divisi mana yang paling cepat merespons, keluhan apa yang paling sering terjadi bulan ini, dan lain-lain.

Apa Dampaknya ke Pembuatan Aplikasi Kamu?

Dengan alur ini, rancangan sistemmu harus memiliki fitur Role-Based Access Control (RBAC). Kamu harus membuat minimal tiga jenis user (hak akses) di dalam sistem:

User (Pegawai Biasa): Hanya bisa membuat tiket dan melihat status tiket miliknya sendiri.

Dispatcher (Admin SDM): Bisa melihat semua tiket baru, menugaskan tiket ke divisi tertentu, dan melihat laporan seluruh divisi.

Resolver (Teknisi Divisi): Hanya bisa melihat tiket yang ditugaskan ke divisinya, mengerjakannya, dan menutup tiket.
