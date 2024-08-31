# **industrialspy3**

pada chall ini saya diberikan sebuah file pcapng

![image](https://github.com/user-attachments/assets/79d9eda9-dd59-42fd-af0e-df8a71f06ee1)

dan sebuah netcat `nc challenges.ctf.compfest.id 9009`

saya mencoba mengecek netcat nya terlebih dahulu

![image](https://github.com/user-attachments/assets/af71bec3-0155-4387-9a74-4b4d46b268cc)

terlihatnya saya akan diberikan beberapa pertanyaan di dalamnya. Saya teringat untuk soal seperti ini, agar memudahkan analisis saya, saya menggunakan online tool bernama
[apackets](https://apackets.com/) yang mana dapat memberikan saya banyak analysis report mengenai pcapng file

Saya coba masukkan file nya ke dalam apackets dan hasilnya seperti dibawah

![image](https://github.com/user-attachments/assets/b9a8316e-d7d8-457b-acec-1f3ad0027658)

saya langsung melihat pada bagian open ports untuk menjawab pertanyaan nya

![image](https://github.com/user-attachments/assets/e536541e-6916-494a-b1bc-05efed13e2f6)

![image](https://github.com/user-attachments/assets/bef9ab17-9a9e-4fa4-8e69-eaa8936a06b5)

saya berhasil menjawab pertanyaan pertama dan lanjut ke pertanyaan selanjutnya. Saya ditanya mengenai credentials yang diakses dalam database. Saya langsung membuka ke bagian credentials

![image](https://github.com/user-attachments/assets/6fa6e7b3-c3f0-4ea7-8bdf-4e2c687b167a)

Karena credentials nya banyak, saya langsung melogikannya. Biasanya credentials yang berhasil untuk mengakses databasenya adalah credential paling akhir dari report.
Karena jika dilihat dari banyak nya credentials ini berarti ada suatu percobaan credentials brute force yang mana brute force nya akan berhenti jika sudah mendapatkan credentials yang tepat yang mana merupakan credentials terakhir yang digunakan

Maka saya langsung pindah ke page credential terakhir untuk menjawab pertanyaannya

![image](https://github.com/user-attachments/assets/913e7462-0aee-4ff2-8ac9-2754a2aa01b3)

![image](https://github.com/user-attachments/assets/1afa1a21-ee53-4da3-932b-34e1d60aefa5)

Saya berhasil menjawab dan lanjut ke pertanyaan selanjutnya yaitu `password` untuk "`super`" user. Disini cukup rumit karena saya harus langsung menganalisis wireshark nya.

Jika saya lihat di apackets, ada percobaan `postgressql` untuk mendapatkan credentials nya

![image](https://github.com/user-attachments/assets/508dfd88-ae1a-46b3-951b-0530a86b5706)

Saya terpikirkan bagaimana jika melakukan searching untuk postgressql pada protocol wiresharknya

![image](https://github.com/user-attachments/assets/b232b0b4-9c40-4c79-b38c-214691bb87e2)

Saya mencoba melakukan analisis pada wireshark dengan memberikan filter `pgsql` dan saya analisis trafficnya satu per satu

![image](https://github.com/user-attachments/assets/ce4cca39-7809-41ff-a2ac-c0f7d30d8ef3)

![image](https://github.com/user-attachments/assets/5f1b37c3-0311-4fe0-9790-8fa4ef0ef541)

ternyata setelah saya coba analisis, saya bisa menemukan "super" user dibawahnya. Dan di gambar kedua, saya menemukan hash untuk passwordnya

![image](https://github.com/user-attachments/assets/54b5745b-5ef9-48ba-88a0-5e09d7cfe24f)

**Hash Password:** `588831adfca19bb4426334b69d9fb49f873e8a22`

Saya mencoba menggunakan `hash identifier` untuk mengecek hash type yang apa yang digunakan pada password ini

![image](https://github.com/user-attachments/assets/c498f2fb-f604-4ca6-b0bc-700e7d3d7028)

Ternyata hash nya adalah `sha1`. Saya langsung mencoba searching di google tool apa saja yang bisa saya gunakan untuk mengdecrypt sha1 ini sampai saya menemukan tool
yang bisa digunakan bernama (md5hashing)[https://md5hashing.net/hash/sha1]

Saya mencoba memasukkan hash nya untuk di decrypt agar bisa menjawab pertanyaan ke 3

![image](https://github.com/user-attachments/assets/faf82994-c27a-4137-aee5-b8be69806667)

![image](https://github.com/user-attachments/assets/9356bc9c-b01c-4060-964b-93930e583cf0)

![image](https://github.com/user-attachments/assets/54762cdf-1352-4e2b-9568-0a4230b335fe)

Saya berhasil menjawabnya. Selanjutnya ditanya `table yang di modify` oleh attacker, saya mencoba analisis line selanjutnya dan langsung menemukan suatu table yang di modify

![image](https://github.com/user-attachments/assets/82f85921-e851-490b-b57f-b00313c29c02)

Saya mencoba mengisi jawabannya dengan `penalties` dan berhasil menjawab pertanyaan ke 4

![image](https://github.com/user-attachments/assets/aabfe101-b03d-4190-a372-92615b77c5c1)

Selanjutnya ditanya `nama lengkap` dari data yang diubah hacker (`nama hacker itu sendiri`) 

Saya mencoba analisis lebih banyak lagi dan menemukan query sql seperti gambar dibawah

![image](https://github.com/user-attachments/assets/8fe7a8da-406d-4830-8937-4515493f97f8)

Dari sini saya bisa mengetahui bahwa dalam table employee, data dari hacker tersebut ada di `id ke 6`. Saya mencoba analisis lebih lanjut lagi dan menemukan beberapa kumpulan nama

![image](https://github.com/user-attachments/assets/0cb3b92e-f4f7-40f8-9275-add919897e71)

Saya melihat apabila salah satu kumpulan nama tersebut adalah "super" user yang disimpan dalam employee table, maka saya menduga bahwa ada nama dari hacker itu sendiri.
Saya mencoba menghitung hingga id ke 6 dan menemukan suatu nama

![image](https://github.com/user-attachments/assets/055f758a-4aee-4e10-8a80-bca63e52970f)

Saya mencoba mengisi dengan nama `Lyubov Pryadko` dan berhasil mendapatkan flag nya

![image](https://github.com/user-attachments/assets/9605fcbf-33f0-4965-b9fd-6116cce53568)

**FLAG:** `COMPFEST16{h3lla_ez_DF1R_t4sK_f0r_4n_1nt3rN_b96818fd79}`
