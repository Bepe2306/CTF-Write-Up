# **Sanity Check**

kalo yang ini kayak biasa aja lah yak, di clue udah langsung dikasih

![image](https://github.com/user-attachments/assets/2f45d425-ec32-4781-b6e0-4374d5c1ea8c)

**FLAG:** `COMPFEST16{gLHF_r3g4rDS_k3ng_nabilmuafa_Zanark_fahrul_tipsen_Maskrio_Ultramy_ultradiyow_PapaChicken_Keego_d7eec71f36}`

# **sigma code**

pada challenge ini saya diberikan sebuah mp3 file

![image](https://github.com/user-attachments/assets/0f295ade-2346-4168-9bbc-4bca7a074689)

Awalnya saya coba memasukkan file ini ke sonic visualizer dan meng add spectogram namun tidak bisa menemukan apa apa. Pada saat saya coba play audionya, ternyata di audio
ini menyebutkan beberapa angka yang saya duga sebagai angka `ASCII value`

Saya langsung saja search di google `mp3 to text converter` dan menemukan tool bernama [notta](https://www.notta.ai/en/tools/audio-to-text-converter).

Saya masukkan mp3 file nya ke dalam web nya dan langsung berhasil mendapatkan `ASCII value` nya, mantappp

![image](https://github.com/user-attachments/assets/f79a0f3f-3bc7-470a-91ad-35e0bb1aa860)

**ASCII VALUE:** `81 48 57 78 85 69 90 70 85 49 81 120 78 110 116 53 78 72 108 102 77 122 86 107 77 68 89 49 77 84 78 107 90 72 48 61`

Saya langsung menggunakan [cyberchef](https://gchq.github.io/CyberChef/) untuk mengdecrypt nya dengan recipe `From Decimal`

![image](https://github.com/user-attachments/assets/bac2bc82-b242-475c-be73-2178a1f7d723)

Ternyata saya masih dapat `Base64` string yang kemudian saya decode lagi dan langsung berhasil mendapatkan flag nya, lets goooo

![image](https://github.com/user-attachments/assets/1783566d-5c4f-4ccc-acab-d9bec22a2720)

**FLAG:** `COMPFEST16{y4y_35d06513dd}`
