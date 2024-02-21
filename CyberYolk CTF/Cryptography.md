# **There Isn’t A Safe Place**

Pada challenge ini saya diberikan sebuah script python.

![place1](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/c0244168-84c7-4e72-93ad-a42970f19521)

Dari description soal yang diberikan dikatakan ”Here is AES for you”, disini saya sebelumnya kurang mengetahui apa itu AES, jadi saya mencoba melakukan searching dan ternyata AES itu adalah sebuah teknik untuk mengencrypt atau decrypt data (Advanced Encryption Standard).

Setelah saya melakukan analisis dari kode yang diberikan dan clue yang diberikan pada description soal, saya langsung mengetahui bahwa saya perlu membuat satu script lagi untuk mengdecrypt pesan yang diberikan dalam file python.

![place2](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/e63d8e4b-29e3-48bf-99a6-472e48baa0f3)

Dari script python ini kemudian saya run pada terminal dan memberikan saya flag dari challenge ini

![place3](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/cc0ff5a1-deaa-4f30-a5dc-b8183b020b0a)

**FLAG:** `CBY{Yes_there_isnt_any_safe_place}`

# **Geser**

Pada challenge ini diberikan sebuah kata kata yang sudah terenkripsi 

![geser1](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/5f32fc4b-8f3b-4c70-9225-e010f0bd828c)

Karena nama challenge nya adalah geser, dari situ langsung memberikan ide apabila kata kata tersebut dienkripsi dengan menggunakan metode Caesar Cipher yang meng shifting kata katanya (geser = shifting). Langsung saya menggunakan tools online https://www.dcode.fr/caesar-cipher untuk meng decode kata kata tersebut yang kemudian memberikan saya flag dari challenge ini

![geser2](https://github.com/Bepe2306/CTF-Write-Up/assets/153899054/da1da339-08e4-4f60-a8a6-9397f8efe5a3)

**FLAG:** `CBY{geser_geser_eh_dapet_flagnya}`
