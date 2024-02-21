# **Where Is She**

Pada challenge ini diberikan sebuah gambar

![she1](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/4170a10c-c9ca-4085-9e3c-25867a4e18d5)

Dari gambar ini, saya harus mencari google plus code, kota, negara bagian dan negara nya. Karena saya sama sekali tidak mengetahui wanita yg ada di dalam foto, saya langsung menggunakan google image untuk mencari tahu.

![she2](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/b8fbf359-429f-48de-bab3-d014c914057f)

Dari google image, saya menemukan nama wanita yang ada di dalam foto. Dikarenakan wanita tersebut terlihat seperti idol KPOP yang mana biasanya mereka mempunyai instagram dan memposting foto mereka disana. Saya mencoba menggunakan instagram untuk mencari info lebih lanjut lagi.

Dari instagram, saya menemukan kemungkinan tempat dari foto diatas dan juga clue lanjutan dari foto lain yang diposting

![she3](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/c733ef24-8dcc-4258-bdf9-c4772094b266)

Dari foto diatas, saya mencoba searching melalui google untuk mencari tempat atau restoran dari background foto diatas.

![she4](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/051d18be-86ef-4ee2-8103-b97c73011603)

Dari clue clue yang sudah saya kumpulkan, saya menggunakan google maps untuk mencari tempat persis dari foto foto diatas. 

![she5](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/bc9e12e5-b6fe-44ad-a56b-c845b352c04d)

Foto diatas setelah saya cari melalui google maps ternyata merupakan background dari foto yang diberikan melalui challenge dan beberapa titik tempatnya juga menyerupai dengan foto foto yang saya temukan di instagram idol KPOP tersebut.

Disini saya cukup yakin bahwa saya sudah menemukan tempat yang benar sehingga saya mencoba mengambil plus code, kota, negara bagian dan negara dari data yang diberikan oleh google maps

![she6](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/dd2655c0-db98-4700-8420-283d0061725b)

Setelah saya mencoba submit sesuai dengan format flag yang diminta, ternyata saya telah menemukan flag yang benar untuk challenge ini

**FLAG:** `CBY{RH3C+4H_Atlanta_ Georgia_USA}`

# **Welcome**
Flag dari challenge ini diberikan langsung di description soal

![welcome1](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/33c6f065-88b6-4591-91d4-49ff4a48a451)

**FLAG:** `CBY{t3t4p_s4Ns_m45iH_1nTr0_To_CtF_g4E5}`

# **A Cow**
Pada challenge ini diberikan sebuah gambar dari suatu tempat

![ragunan1](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/f32465c2-eded-4011-88dc-b6284820286c)

Disini saya disuruh untuk mencari tempat berdasarkan gambar yang diberikan. Saya menggunakan google image untuk menelusuri tempat tersebut

![ragunan2](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/b5f2b315-abd3-448f-981e-c0a27b0b6eee)

Dari sini saya langsung mengetahui bahwa tempat dari gambar yang diberikan adalah Kebun Binatang Ragunan. Karena challenge ini mau kita untuk memberikan nama tempat, nama kecamatan dan nama kota. Saya mencoba googling lokasi detail dari Ragunan. 

![ragunan3](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/c386a064-84bd-41b2-a9d1-276a2f2571c8)

Maka flag dari challenge ini akan menjadi:

**FLAG:** `CBY{ragunanpasarminggujakartaselatan}`

# **Alienated**
Pada challenge ini, diberikan sebuah file txt yang berisi kata kata dibawah

![alien1](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/83b4f98f-2f95-4b74-a20d-6a4dd6081b0a)

Dari bentukan kata kata tersebut, terlihat apabila kata kata tersebut di enkripsi menggunakan base64. Langsung saya menggunakan tools online https://www.base64decode.org/ untuk mengdecode kata katanya

![alien2](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/a62b56fc-108f-491f-b752-7a8fb3eb5441)

Disini flag sudah muncul sebagian, namun beberapa masih terenkripsi dengan simbol yang cukup aneh. Dikarenakan nama challenge ini adalah alienated, maka saya mencoba untuk melakukan decryption menggunakan alien language dengan tools online https://lingojam.com/AlienLanguage, dan yang saya decode hanya bagian alien language nya saja dan memberikan hasil dibawah

![alien3](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/e6255e36-b6b0-498b-86dd-3e9191c37cd1)

Sehingga flag dari challenge ini adalah

**FLAG:** `CBY{A14_TrY1n9_t0_eat_pr4wn-with_sauce}`
