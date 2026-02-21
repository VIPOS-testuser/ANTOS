

# 🐜 ANT OS  | The Ghost in the RAM

**ANT OS** — bu kiberxavfsizlik mutaxassislari, Red Team operatorlari va maxfiylik ishqibozlari uchun maxsus ishlab chiqilgan, minimalistik, RAM-only (faqat tezkor xotirada ishlovchi) Linux distributivi. Tizimning asosiy falsafasi: **"Hech qanday iz qoldirmaslik va maksimal tezlik"**.

---

## 🧐 ANT OS nima?

ANT OS — bu an'anaviy operatsion tizimlardan farqli o'laroq, diskka emas, balki to'liq operativ xotiraga yuklanuvchi yengil muhitdir. U sizga bir martalik operatsiyalarni amalga oshirish, tizimlarni test qilish va muhim topshiriqlarni xavfsiz bajarish uchun xizmat qiladi.

## ⚔️ Qo'llaniladigan Hujum va Operatsiya Turlari (Red Teaming)
### 🎯 Nimalar qilish mumkin?  
Quyidagi keltirilganlar shunchaki misol sifatida keltiriligan va bularni bajarish uchun sizdan bash script talab qilinadi va uni o'zingiz yozishingiz kerak bo'ladi.
OS turli xildagi payloadlarni genaratsiya ham qilamyadi shunchaki ularni qo'llash yokida o'rnatish uchun yordamchi vositadir.


* **Unauthorized USB / Flash Attack:**  
  Hujumchi tashqi fleshka yoki bootable qurilma ulab, tizimni chetlab o‘tish, boshqa muhitdan yuklash yoki ma’lumotlarni o‘g‘irlashga urishi.

* **System File Modification:**  
  Muhim tizim fayllarini almashtirish, buzish yoki yashirincha o‘zgartirib qo‘yish orqali tizim ishlashini izdan chiqarish.

* **Offline Data Theft:**  
  Tizim o‘chirilgan holatda diskdagi ma’lumotlarni o‘qish, nusxalash yoki tashqi qurilmaga ko‘chirib olish urinishlari.

* **DLL Hijacking / Injection:**  
  Qonuniy dasturlar ishlatadigan DLL fayllarni almashtirish yoki ularni zararli komponentlar bilan yuklash orqali tizimni nazorat qilishga urinish.

* **Persistence Installation:**  
  Tizim yuklanganda avtomatik ishga tushadigan yashirin skriptlar, servislar yoki komponentlarni joylashtirib ketish.

* **Live Memory Data Theft:**  
  Ishlayotgan tizim RAM’idan vaqtinchalik va sezgir ma’lumotlarni o‘g‘irlashga urinishlar.

* **Boot Process Tampering:**  
  Bootloader yoki tizim yuklanish zanjiriga aralashib, tizimni hujumchi xohishiga ko‘ra yuklashga urinish.

* **Forensic Trace Removal:**  
  Hujumdan so‘ng izlarni yashirish, loglarni o‘chirish yoki tizimni “toza” holatda qoldirishga urinishlar.

---

## 🔐 Maxfiylik va Stealth Darajalari

ANT OS o'rnatish vaqtida sizga quyidagi operatsion xavfsizlik (OPSEC) darajalarini taklif qiladi:

| Daraja | Nomi | Texnik tavsifi | OPSEC darajasi |
| :--- | :--- | :--- | :--- |
| **Level 1** | **Open Field** | Hamma narsa bitta FAT32 bo'limda. Fayllar Windows/Linuxda ochiq ko'rinadi. | 🟢 Past |
| **Level 2** | **Hybrid Ghost** | Tizim yashirin bo'limda, ma'lumotlar (Data) bo'limi ochiq. Skriptlar tashqaridan boshqariladi. | 🟡 O'rta |
| **Level 3** | **Black Hole** | Tizim va `1.sh` payload to'liq yashirin. Flashka "unallocated" bo'lib ko'rinadi. | 🔴 Yuqori |

---

## 🛠 O‘rnatish va Ishga Tushirish (Installation)

Defender minimal resurslarda ishlashga mo‘ljallangan bo‘lib, tezkor va xavfsiz ishga tushiriladi.

### 📋 Tizim Talablari:
* Kamida **512 MB RAM** ga ega kompyuter
* **1 GB yoki undan katta** USB Flash qurilma
* O‘rnatish uchun **Linux o‘rnatilgan asosiy kompyuter**

---

### 🚀 O‘rnatish Qadamlari:

1. **Repozitoriyani klonlash:**
   ```bash
   git clone https://github.com/VIPOS-testuser/ANTOS.git
   ```
2. **UnZip qilish:**
   ```bash
   unzip ant.zip -d ANTOS
   ```
3. **ANTOS papkasi ichiga kirish:**
   ```bash
      cd ANTOS/ant/
   ```
   
4. **O‘rnatish skriptiga ruxsat berish:**
   ```bash 
   sudo chmod +x installer.sh
   ```
5. **Installerni ishga tushirish:**
   ```bash
   sudo ./installer.sh
   ```
⚠️ **Eslatma:**  
O‘rnatish jarayonida installer sizdan:
* USB flash qurilmani tanlash
* Maxfiylik (security) darajasini belgilash
* Avtomatik ishga tushiriladigan `.sh` skript yo‘lini ko‘rsatish  
talab qiladi.

---


## 📜 Axloqiy Chegara va Mas'uliyat (Disclaimer)

⚠️ **DIQQAT:** ANT OS loyihasi faqat ta'lim, kiberxavfsizlik tadqiqotlari va qonuniy penetratsion testlar uchun mo'ljallangan.

1. **Axloqiy Chegara:** Tizimdan begona shaxslar yoki tashkilotlarning ruxsatisiz ularning infratuzilmasiga hujum qilish uchun foydalanmang.
2. **Mas'uliyat:** Har bir foydalanuvchining erki o'zida. Ushbu vositadan foydalanish natijasida kelib chiqadigan har qanday qonuniy yoki moddiy zarar uchun loyiha yaratuvchisi **javobgar emas**.
3. **Eslatma:** Ushbu OS "as is" (boricha) holatida taqdim etiladi va uning ishlashi yoki xavfsizligiga 100% kafolat berilmaydi.

---

**ANT OS** — Invisible. Inevitable. 🐜
