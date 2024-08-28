# **Random**

pada challenge ini saya diberikan code seperti ini

![image](https://github.com/user-attachments/assets/b0157b0a-a8cc-4134-b84c-95796dca5410)

jika dilihat dari code, code ini akan membuat random byte dari flag challenge ini. Namun jika saya coba proses dengan template flag nya yaitu `COMPFEST{` lalu saya
tambahi lagi inputan asal menjadi `COMPFEST{1` atau `COMPFEST{12`, ternyata byte nya tidak benar benar random seperti gambar dibawah

![image](https://github.com/user-attachments/assets/0d64aebe-6d7e-4560-8251-91a93dd9e92a)

dari sini saya memiliki ide untuk membuat python script yang mana dapat melakukan brute force pada random byte nya sehingga saya dapat menebak flag dari chall ini

![image](https://github.com/user-attachments/assets/7c79b1a7-4c28-4abf-9449-0e5ad8dfffb5)

Penjelasan singkat script:

- `import random`: tentunya perlu mengimport library random agar bisa menebak random bytenya
- `start`: place holder untuk flag nya
- `alphanumeric`: saya memasukkan semua possible alphanumeric yang ada di dalam flag dari angka `0-9`, alphabet `a-z` dan `A-Z` serta memasukkan `{` dan `}`
  yang merupakan bagian dari flag nya (membuka dan menutup flag)
- `target`: target byte yang ingin dituju agar kita bisa melihat apakah byte flag kita sudah sesuai dengan byte target
- `for loop`: memutar loop dari start flag dengan i yang di looping dalam alphanumericnya, apabila sudah ditemukan alphabet yang byte nya sesuai target,
  alphabeth tersebut akan di store ke bagian start kemudian berjalan lagi for loop nya
  ![image](https://github.com/user-attachments/assets/a771d704-6ac8-47db-affb-e88d869e6329)

  
pada saat penjalanan script pun terkadang byte yang ditebak bisa tidak sesuai sehingga saya harus memasukkan alphabet yang sudah sesuai ke dalam start secara manual
ataupun saya harus menebaknya satu persatu byte yang sesuai kemudian saya masukkan ke start nya kembali secara manual

dari proses automation dan debugging secara manual tersebut akhirnya saya berhasil menemukan flag nya

![image](https://github.com/user-attachments/assets/30310e2b-271a-4078-b80d-0c9dfe1dd9e1)

**FLAG:** `COMPFEST16{C0mpu73r_c0uld_n0t_m4k3_Tru3_R4nd_0be49a7429}`
