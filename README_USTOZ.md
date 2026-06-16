# NLP Kasbiy malaka oshirish kursi — Ko'rib chiqish paketi

**Kurs nomi:** Tabiiy tilni qayta ishlash (NLP) — Kasbiy malaka oshirish
**Muddati:** 15-iyun – 10-iyul 2026 (16 o'quv kuni, dushanba/seshanba/payshanba/juma)
**Jadval:** 09:30–10:50 Amaliyot · 11:00–12:20 Ma'ruza · Chorshanba Milestone (asinxron)
**O'qituvchilar:** I.R. Atadjanov (amaliyot) · A.A. Abdulali (ma'ruza)

---

## Bu paket nimani o'z ichiga oladi

Bu paket kursning tinglovchilarga mo'ljallangan barcha materiallarini o'z ichiga oladi.
Ishlab chiqarish tizimi (skriptlar, AI-konfiguratsiya fayllari) kiritilmagan.

---

## Papkalar tuzilmasi

```
README_USTOZ.md          ← shu fayl
course_map.yaml          ← 16 kunlik jadval va mavzular ro'yxati
LICENSES.md              ← barcha ma'lumotlar to'plamlari litsenziyalari
requirements.txt         ← Python paketlari (Kaggle muhitiga mos)

lectures/                ← Ma'ruza slaydlari
  d01_nlp_asoslari.tex   │  LaTeX manba fayli (Overleaf da kompilyatsiya qiling)
  d01_nlp_asoslari.pdf   │  Tayyor PDF
  d02_klassik_tasnif.tex │  (PDF hali yo'q — Overleaf da kompilyatsiya kerak)
  d03_vektor_embedding.*
  d04_qidiruv_imlo.*

practices/               ← Amaliyot daftarlari (Kaggle Notebooks da ishlatiladi)
  d02_p1_preprocessing.ipynb          Tinglovchi variantı (bo'sh joylar bor)
  d02_p1_preprocessing_SOLUTIONS.ipynb  Javob kaliti
  d03_p2_sentiment.*
  d04_p3_embeddings.*
  d02_checkpoints/       Offline ma'lumotlar (internet bo'lmasa ishlatiladi)
  d03_checkpoints/
  d04_checkpoints/

capstone/                ← Kapstone loyiha hujjatlari
  SPEC.md                  Loyiha shartnomasi va umumiy tavsif
  contracts.py             Barcha modullar uchun Python imzolari (type hints)
  modules/
    m01_text_preprocessor.py   1-kun dan keyin tinglovchi yozadi
    m02_sentiment_classifier.py
    m03_pretrained_embedder.py

day1_orientation/        ← 1-kun: Orientatsiya
  d01_kirish.tex / .pdf    Orientatsiya slaydlari
  d01_orientatsiya.ipynb   Muhit tekshiruvi daftari (Kaggle da bajariladi)
  HISOB_YARATISH.md        Kaggle/HuggingFace/GitHub hisoblarini ochish yo'riqnomasi
  pre_course.docx / .xlsx  Oldindan ko'rib chiqish uchun materiallar

assessments/             ← Kurs oldi va kurs ichi baholash materiallari
milestones/              ← Haftalik milestone topshiriqlari (to'ldirilmoqda)
```

---

## .tex fayllarni qanday kompilatsiya qilish (Overleaf)

1. **overleaf.com** → *New Project → Upload Project*
2. `.tex` faylini yuklang
3. *Recompile* tugmasini bosing (pdfLaTeX, ikki marta)
4. PDF yuklab olinadi

Barcha `.tex` fayllar o'z-o'ziga yetarli (tashqi `\input` yo'q).
Zarur paketlar: `beamer`, `tcolorbox`, `tikz`, `listings`, `booktabs`, `lmodern`
(Overleaf da barchasi mavjud).

---

## Amaliyot daftarlarini qanday ishlatish (Kaggle)

1. **kaggle.com** → *Create Notebook → File → Import Notebook*
2. `.ipynb` faylini yuklang
3. *Run All* (`Shift+Enter` yoki *Run All*)
4. Birinchi katakda `OFFLINE_FALLBACK = True` — internet bo'lmasa ham ishlaydi

Har daftarning birinchi bo'limida zarur paketlar o'rnatiladi.

---

## Eslatmalar ko'rib chiquvchiga

- **Tinglovchi varianti** va **javob kaliti** (`_SOLUTIONS`) har bir amaliyot uchun alohida berilgan.
- Daftarlardagi `assert` satrlari tinglovchining to'g'ri javob yozganini avtomatik tekshiradi.
- Kapstone loyiha har hafta bitta modul bilan to'ldirib boriladi; `capstone/modules/` papkasida
  allaqachon tayyor modullar (m01–m03) namuna sifatida berilgan.
- `course_map.yaml` — jadval, mavzular, o'lchanadigan maqsadlar va har kungi qo'lda
  hisoblangan namunaviy sonlar uchun yagona manba.
