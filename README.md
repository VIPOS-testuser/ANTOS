

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


## 🛠 O'rnatish va Ishga tushirish (Installation)

### 📋 Talablar:
* Kamida 512MB RAMga ega kompyuter.
* 1GB yoki undan katta flashka.
* Linux o'rnatilgan asosiy kompyuter (O'rnatish uchun).

### 🚀 O'rnatish qadamlari:
1. Repozitoriyani klonlang:
   ```bash
   git clone [https://github.com/sizning_nik/ant-os.git]

    Unauthorized USB Boot & Flash Attack:
    Hujumchi tashqi fleshka yoki bootable media ulab, tizimni chetlab o‘tish, o‘zgartirish yoki boshqa OS orqali ma’lumotlarni o‘g‘irlashga urishi.

    System File Tampering Attack:
    Muhim tizim fayllarini almashtirish, patch qilish yoki yashirincha o‘zgartirib qo‘yish orqali tizim xatti-harakatini buzish.

    Offline Data Theft:
    Tizim o‘chirilgan holatda diskni o‘qish, nusxa ko‘chirish yoki sezgir ma’lumotlarni tashqi qurilmaga ko‘chirish urinishlari.

    DLL Replacement & Injection Attack:
    Qonuniy dasturlar ishlatadigan DLL fayllarni almashtirish yoki jarayon ichiga soxta kutubxonalarni yuklash orqali nazorat o‘rnatish.

    Persistence Implantation:
    Tizim yuklanganda avtomatik ishga tushadigan yashirin skriptlar, servislar yoki triggerlarni joylashtirib ketish.

    Memory Scraping & Live Data Capture:
    Ishlayotgan tizim RAM’idan vaqtinchalik ma’lumotlarni (kalitlar, sessiyalar, konfiguratsiyalar) tortib olishga urinishlar.

    Boot Chain Manipulation:
    Bootloader yoki pre-OS komponentlariga aralashib, tizimni hujumchi nazoratida yuklash.

    Forensic Footprint Cleanup by Attacker:
    Hujumdan so‘ng izlarni yo‘qotish, loglarni o‘chirish yoki tizimni “toza ko‘ringan” holatga keltirish urinishlari.
(https://github.com/VIPOS-testuser/ANTOS.git)
   cd ant-os
   ```
2. O'rnatish skriptiga ruxsat bering:
```bash
sudo chmod +x install.sh
```
3. Installerni ishga tushiring:
```bash
sudo ./install.sh
```


*Installer sizdan flashka raqamini, maxfiylik darajasini va ishga tushuvchi `.sh` skriptingiz yo'lini so'raydi.*

---

## 📜 Axloqiy Chegara va Mas'uliyat (Disclaimer)

⚠️ **DIQQAT:** ANT OS loyihasi faqat ta'lim, kiberxavfsizlik tadqiqotlari va qonuniy penetratsion testlar uchun mo'ljallangan.

1. **Axloqiy Chegara:** Tizimdan begona shaxslar yoki tashkilotlarning ruxsatisiz ularning infratuzilmasiga hujum qilish uchun foydalanmang.
2. **Mas'uliyat:** Har bir foydalanuvchining erki o'zida. Ushbu vositadan foydalanish natijasida kelib chiqadigan har qanday qonuniy yoki moddiy zarar uchun loyiha yaratuvchisi **javobgar emas**.
3. **Eslatma:** Ushbu OS "as is" (boricha) holatida taqdim etiladi va uning ishlashi yoki xavfsizligiga 100% kafolat berilmaydi.

---

**ANT OS** — Invisible. Inevitable. 🐜
