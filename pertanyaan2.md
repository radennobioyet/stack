# JOBSHEET STACK

# Percobaan 1

Pertanyaan
1.	Jelaskan alur kerja dari method konversiDesimalKeBiner!
2.	Pada method konversiDesimalKeBiner, ubah kondisi perulangan menjadi while (kode != 0), bagaimana hasilnya? Jelaskan alasannya!


Jawaban
1. Alur Kerja Method konversiDesimalKeBiner
Method ini bekerja dengan menerapkan prinsip Last In First Out (LIFO) dari struktur data Stack untuk mengubah bilangan desimal menjadi biner melalui serangkaian pembagian. Pertama, nilai desimal dibagi dua secara berulang, di mana sisa baginya (0 atau 1) dimasukkan (push) ke dalam stack hingga nilai desimal habis menjadi nol. Setelah semua sisa bagi terkumpul, program akan mengeluarkan (pop) data tersebut satu per satu dari stack dan menyambungkannya ke dalam sebuah string; karena sisa bagi yang terakhir masuk adalah angka biner yang paling signifikan, proses pengeluaran ini secara otomatis membalikkan urutan angka sehingga membentuk susunan biner yang tepat dari depan ke belakang.

2. Analisis Perubahan Kondisi while (nilai != 0)
Jika kondisi perulangan diubah menjadi while (nilai != 0), hasil output untuk bilangan positif akan tetap sama karena baik kondisi "lebih dari nol" maupun "tidak sama dengan nol" akan sama-sama berhenti ketika nilai mencapai angka nol setelah pembagian berulang. Namun, secara teknis penggunaan != 0 lebih berisiko jika program menerima input bilangan negatif karena perulangan akan terus berjalan mengikuti logika pembagian bilangan negatif yang tidak sesuai dengan algoritma biner sederhana ini, sedangkan kondisi > 0 berfungsi sebagai pengaman agar algoritma hanya memproses bilangan positif sesuai dengan logika sisa bagi yang standar.
