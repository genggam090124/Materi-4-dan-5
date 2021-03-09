# Materi-4-dan-5
Fragment merupakan salah satu komponen pada Android Studio dengan fungsi yang hampir sama seperti activity tetapi memiliki “lifecycle” yang berbeda.
Fragment merupakan bagian dari sebuah activity yang mana sebuah fragment tidak akan ada bila tidak ada sebuah activity karena fragment membutuhkan 
akses dari activity untuk dapat dijalankan.
Fragment berisi method callback mirip dengan Activity, seperti onCreate (), onStart (), onPause (), dan OnStop (). 
Siklus hidup dari fragment berhubungan dengan siklus hidup Activity, berikut tahapan siklus hidup fragment yang berkaitan dengan siklus hidup dari activity.
Fragmen harus selalu tersemat dalam aktivitas dan daur hidup fragmen secara langsung dipengaruhi oleh daur hidup aktivitas host-nya. Misalnya, saat aktivitas dihentikan sementara, semua fragmen di dalamnya juga dihentikan sementara, dan bila aktivitas dimusnahkan, semua fragmen juga demikian. Akan tetapi, saat aktivitas berjalan (dalam status daur hidup dilanjutkan), bisa memanipulasi setiap fragmen secara terpisah, seperti menambah atau membuangnya. Saat melakukan transaksi fragmen, Anda juga bisa menambahkannya ke back-stack yang dikelola oleh aktivitas—setiap entri back-stack merupakan catatan transaksi fragmen yang terjadi. Dengan back-stack pengguna dapat membalikkan transaksi fragmen (mengarah mundur), dengan menekan tombol Kembali. menambahkan fragmen sebagai bagian dari layout aktivitas, fragmen tersebut berada di ViewGroup di dalam hierarki tampilan aktivitas dan fragmen menentukan layout tampilannya sendiri. Anda bisa menyisipkan fragmen ke dalam layout aktivitas dengan mendeklarasikan fragmen dalam file layout aktivitas, sebagai elemen <fragment>, atau dari kode aplikasi dengan menambahkannya ke ViewGroup yang ada. 

 Fragments merupakan content controllers dan memiliki view, layout, serta event logic sendiri
- Lifecycle pada Fragment 
- OnAttach, saat sebuah fragment dipanggil sebuah activity
- OnCreate, dipanggil untuk pembuatan awal fragment
- OnCreateView, memanggil karna saat itu sistem sedang menggambar fragment pertama kali
- OnActivityCreated, dipanggil ketika activity telah selesai dengan method onCreate
- OnStart, dipanggil karna fragment telah siap untuk didisplay atau ditampilkan di layar
- OnResume, digunakan untuk membuat fragment interaktif.
- OnDetach, fragment tidak terikat dengan activity, dan tidak memiliki hirarki view lagi.
- OnDestroy, dipanggil setelah fragment tidak digunakan, masih ada objek java melekat pada activity.
- OnDestroyView, dipanggil setelah hirarki view fragment tidak lagi dapat diakses.
- OnStop, digunakan jika fragment tidak lagi  terlihat.
- OnPause, sistem akan memanggil metode ini sebagai indikasi pertama bahwa pengguna sedang meninggalkan fragmen(walau itu tidak selalu berarti fragmen sedang dimusnahkan)

Kelebihan :

-.Tidak perlu memasukkan nama file fragment ke dalam “AndroidManifest” yang diperlukan oleh activity.

-.Fungsi yang berada pada activity dapat langsung digunakan dalam fragment tersebut tanpa harus membuat ulang. 
  Contoh: pada saat back, fragment hanya perlu memanggil fungsi “getactivity
  
