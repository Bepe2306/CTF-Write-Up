# **Phoenix Flower**

Pada challenge ini diberikan sebuah file yang bernama “Phoenix_Flower.wav”. Dari extension file wav tersebut, saya langsung mengetahui bahwa file ini berisi sebuah rekaman suara atau audio spectrogram. Maka saya langsung membuka app Sonic Visualizer untuk melihat spectrogram audio dari file tersebut.


Setelah saya memasukkan file Phoenix_Flower.wav tersebut, awalnya akan terbentuk seperti gambar dibawah

![foren1](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/d34bd498-1225-4a63-b965-4a893f798b1e)


Jika sudah seperti ini saya hanya perlu menambahkan spectrogram melalui menu ‘Pane’ yang akan memberikan saya flag dari challenge ini

![foren2](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/03268c4c-ae2f-46ef-b207-a8665b441099)

**FLAG:** `CBY{He4L1Ng_FOR_3vERyONe}`

# **Sound Mystery**

Pada challenge ini diberikan sebuah file bernama “Sound Mystery.wav”. Awalnya saya pikir challenge ini akan sama saja dengan challenge sebelumnya, namun dari deskripsi challenge yang diberikan, terlihat cukup berbeda dengan chall sebelumnya, tapi saya mencoba melakukan scanning spectrogram dengan Sonic Visualizer untuk memastikan kembali.


Namun setelah dilakukan scanning, benar saja bahwa challenge ini cukup berbeda dengan challenge sebelumnya karena pada spectrogram tidak menghasilkan audio sama sekali. Dari situ, saya langsung mencoba binwalk file untuk melihat isi dari file tersebut dan ditemukan file zip di dalamnya.


![foren3](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/a87b1b2c-0dcc-4758-afda-fd68cf1cb57e)

Dari situ saya mencoba untuk mengextract file tersebut dan ditemukan dua file yaitu ‘D757C.zip’ dan ‘whale.jpg’. Dikarenakan dari description soal dikatakan ‘Legend has it that it lies beneath a huge whale’, saya mencoba untuk melakukan steganography pada file whale.jpg dengan menggunakan stegsolve. Tapi dari steganography tersebut, saya tidak dapat menemukan clue ataupun flag.

Disini saya agak sedikit kebingungan, tapi saya penasaran apabila di dalam file whale.jpg ini masih ada file lainnya, sehingga saya mencoba binwalk lagi dan benar saja di dalam whale.jpg itu terdapat banyak sekali zip file.


![foren4](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/35c60248-2606-4946-b8c7-288f27ce4312)

Dari sini saya langsung melakukan extract pada whale.jpg yang kemudian saya mencoba masuk ke dalam directory - directory yang ada dalam file tersebut yang membawa saya pada bagian dibawah


![foren5](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/d5f1377c-88bf-44b8-b2f8-669093a28734)

Disini saya cukup kebingungan, karena terdapat banyak sekali directory yang dapat dimasukki dan apabila saya masuki satu satu tentunya akan sangat memakan waktu. Maka dari itu saya mencoba melakukan analisis terlebih dahulu pada directory nomor 1 untuk melihat isi dari semua directory itu kurang lebih bagaimana.

Di dalam directory tersebut terdapat 3 directory lagi seperti gambar dibawah


![foren6](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/73bee7af-0788-45f1-a6df-8c758c831cbf)

Yang masing masing dari directory ini memiliki 3 file.txt seperti dibawah


![foren7](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/01b50c14-a222-4031-98d2-22d0284465ef)

Saya mencoba cat masing masing file.txt ini dan memberikan saya hasil sebagai berikut


![foren8](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/bc4442d2-c99f-4323-9898-b6260a9d263c)

Disini saya cukup kebingungan cara untuk mengambil flagnya bagaimana karena directory yang harus dikunjungi cukup banyak. Saya mencoba mencari info cara untuk mengunjungi directory tersebut satu per satu secara otomatis dan bisa juga mendapatkan flag dari challenge ini. Setelah saya coba cari, saya menemukan satu cara yang menarik.

Dari prediksi yang saya lakukan, setiap file.txt yang ada di dalam tiap directory akan memberikan kata ‘No flag here but... I don't know :)’. Maka saya akan mencoba memberikan command grep namun memberikan option -v yang dimana command grep akan mengambil kata kata yang diinginkan selain dari kata kata yang dimasukkan ke dalam option -v. 

Lalu saya juga memberikan option -r yang berfungsi sebagai recursive, dengan memberikan path folder saya pada option -r tersebut maka directory akan dikunjungi satu satu secara otomatis sehingga command yang dijalankan akan menjadi seperti:

`grep -v "No flag here but... I don't know :)" -r /home/kali/Downloads/_sound_mystery.wav.extracted/_whale.jpg.extracted/zipchall/folders`

Dari command ini saya berhasil mendapatkan flag dari challenge ini


![foren9](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/c924963b-06e6-4924-9a16-0a2c09c943e0)

**FLAG:** `CBY{4ud10_70_1M4g3_70_Fl4G}`
