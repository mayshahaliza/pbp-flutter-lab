# counter_7

A new Flutter project.

## Getting Started

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://docs.flutter.dev/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://docs.flutter.dev/cookbook)

For help getting started with Flutter development, view the
[online documentation](https://docs.flutter.dev/), which offers tutorials,
samples, guidance on mobile development, and a full API reference.

TUGAS 7
1. Jelaskan apa yang dimaksud dengan stateless widget dan stateful widget dan jelaskan perbedaan dari keduanya.
2. Sebutkan widget apa saja yang kamu pakai di proyek kali ini dan jelaskan fungsinya.
3. Apa fungsi dari setState()? Jelaskan variabel apa saja yang dapat terdampak dengan fungsi tersebut.
4. Jelaskan perbedaan antara const dengan final.
5. Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas.

Jawab:
1. - Stateless widget: tidak mempunyai state. Dapat berubah hanya oleh event eksterenal dalam parent widget dari widget tersebut. Child widget mendapatkan deskripsi dari parent widgetnya dan tidak dapat mengubahnya sendiri. Hanya mempunyai properti yang bersifat final.
   - Stateful widget: dapat mengubah deskripsi secara dinamis. Mempunyai company state class yang merepresentasikan state dari widget sekarang.
2. Floating action button (tombol + dan - untuk increment dan decrement), Container, Column, dan Row untuk penyesuaian letak widget, Text untuk menampilkan teks, dan Scaffold untuk mengimplementasikan struktur tata letak visual desain material dasar
3. setState() digunakan saat mengganti internal state dari objek State (saat meng-update data model user interface). setState() digunakan untuk memberitahu framework jika internal state dari objek tersebut sudah berubah.
4. - Final: digunakan untuk mendeklarasikan variabel yang immutable (tidak dapat diubah) yang nilai variabelnya sudah atau belum diketahui (nilai final diketahui saat run time)
   - Const: digunakan untuk mendeklarasikan variabel yang immutable yang nilai variabelnya sudah di-assign di awal (nilai const harus sudah diketahui saat compile time)
5. - Create app (flutter create counter_7) dan membuka main.dart
    - Mengganti title di const MyHomePage menjadi Program Counter
    - Menambahkan widget yakni floating action button - yang berfungsi untuk decrement dan + untuk increment. Button - di-set untuk hanya muncul jika counter lebih dari 0
    - Menyesuaikan tampilan tulisan ganjil dan genap sesuai dengan logika yang diminta (warna di-set dengan TextStyle)

REFERENSI
- https://alvinalexander.com/flutter/setState-method-explained/
- https://api.flutter.dev/flutter/widgets/State/setState.html
- https://codekey.id/dart/flutter-scaffold/

TUGAS 8
1. Jelaskan perbedaan Navigator.push dan Navigator.pushReplacement.
2. Sebutkan widget apa saja yang kamu pakai di proyek kali ini dan jelaskan fungsinya.
3. Sebutkan jenis-jenis event yang ada pada Flutter (contoh: onPressed).
4. Jelaskan bagaimana cara kerja Navigator dalam "mengganti" halaman dari aplikasi Flutter.
5. Jelaskan bagaimana cara kamu mengimplementasikan checklist di atas.

Jawab:
1. Navigator.push menambahkan page baru di atas navigation stack. Navigator.pushReplacement me-replace screen teratas pada stack dengan page yang baru.
2. Container, Column, dan Row untuk penyesuaian letak widget, Text untuk menampilkan teks, dan Scaffold untuk mengimplementasikan struktur tata letak visual desain material dasar
3. onPressed, onLongPress, onTap, onChanged, dsb.
4. Navigator mengatur page mana yang akan ditampilkan serta mengatur pergantian/penambahan page. Struktur navigator berupa stack, di mana page teratas adalah yang muncul. Penggantian halaman dilakukan dengan pemanggilan Navigator.pushReplacement. Tidak seperti Navigator.push yang langsung menambahkan halaman baru di atas stack, Navigator.pushReplacement me-remove halaman teratas pada stack terlebih dahulu kemudian menambahkan halaman yang baru pada stack.
5. - Menambahkan drawer dan membuat navigasi counter_7, tambah dan data budget di drawer serta menggunakan Navigator.pushReplacement untuk mengganti page
    - Menambahkan halaman form, dengan string judul, int nominal, dan dropdown menu dengan Padding() dan button

REFERENSI
https://www.technicalfeeder.com/2021/11/flutter-page-transition/