# JOBSHEET STACK

# Percobaan 1

Pertanyaan

1.  Lakukan perbaikan pada kode program, sehingga keluaran yang dihasilkan sama dengan verifikasi hasil percobaan! Bagian mana yang perlu diperbaiki?
2.  Berapa banyak data tugas mahasiswa yang dapat ditampung di dalam Stack? Tunjukkan potongan kode programnya!
3.  Mengapa perlu pengecekan kondisi !isFull() pada method push? Kalau kondisi if-else tersebut dihapus, apa dampaknya?
4.  Modifikasi kode program pada class MahasiswaDemo dan StackTugasMahasiswa sehingga pengguna juga dapat melihat mahasiswa yang pertama kali mengumpulkan tugas melalui operasi lihat tugas terbawah!
5.  Tambahkan method untuk dapat menghitung berapa banyak tugas yang sudah dikumpulkan saat ini, serta tambahkan operasi menunya!
6.      Commit dan push kode program ke Github

Jawaban

1.

```
public void print() {
        for (int i = top; i >= 0; i--) {
            System.out.println(stack[i].nama + "\t" + stack[i].nim + "\t" + stack[i].kelas);
        }
        System.out.println("");
    }
```

2. ada 5

```
StackTugasMahasiswa19 stack = new StackTugasMahasiswa19(5);
```

3. untuk mencegah terjadinya Stack Overflow, yaitu kondisi error ArrayIndexOutOfBoundsException yang muncul saat program mencoba memasukkan data baru ke dalam array yang sudah mencapai batas kapasitas maksimalnya. Dengan adanya validasi ini, program dapat tetap berjalan stabil karena pointer top akan selalu terjaga di dalam rentang indeks yang valid, sekaligus memungkinkan sistem untuk memberikan peringatan informatif kepada pengguna alih-alih mengalami crash atau berhenti secara mendadak.

4.
StackTugasMahasiswa19
```
public Mahasiswa19 peekBottom() {
        if (!isEmpty()) {
            return stack[0];
        } else {
            System.out.println("Stack kosong!");
            return null;
        }
    }
```


MahasiswaDemo19
```
case 5:
                    Mahasiswa19 lihatBawah = stack.peekBottom();
                    if (lihatBawah != null) {
                        System.out.println("Tugas pertama dikumpulkan oleh: " + lihatBawah.nama);
                    }
                    break;
```

5. StackTugasMahasiswa19
```
public int getCount() {
    return top + 1;
}
```

MahasiswaDemo19
```
case 6:
                    System.out.println("Jumlah tugas saat ini: " + (stack.top + 1));
                default:
                    System.out.println("Pilihan tidak valid.");
         while (pilih >= 1 && pilih <= 6);
```

6. done