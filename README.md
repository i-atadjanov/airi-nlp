# NLP Kasbiy malaka oshirish kursi — Ko'rib chiqish paketi

**Kurs nomi:** Tabiiy tilni qayta ishlash (NLP) — Kasbiy malaka oshirish
**Muddati:** 15-iyun – 10-iyul 2026 (16 o'quv kuni, dushanba/seshanba/payshanba/juma)
**Jadval:** 09:30–10:50 Amaliyot · 11:00–12:20 Ma'ruza · Chorshanba Milestone (asinxron)
**O'qituvchilar:** I.R. Atadjanov (amaliyot) · A.A. Abdulali (ma'ruza)

---

## Bu paket nimani o'z ichiga oladi

Bu paket kursning tinglovchilarga mo'ljallangan barcha materiallarini o'z ichiga oladi.
Ishlab chiqarish tizimi (skriptlar, AI-konfiguratsiya fayllari) kiritilmagan.

**Holat (16-iyun 2026):** 1–3-haftalar to'liq tayyor (kunlar 1–12, milestonelar w1–w3).
4-hafta (kunlar 13–16: Transformer, fine-tuning, RAG/agentlar, joylashtirish) ishlanmoqda.

---

## Papkalar tuzilmasi

```
README_USTOZ.md          <- shu fayl
course_map.yaml          <- 16 kunlik jadval va mavzular ro'yxati
LICENSES.md              <- barcha ma'lumotlar to'plamlari litsenziyalari
requirements.txt         <- Python paketlari (Kaggle muhitiga mos)

lectures/                <- Ma'ruza slaydlari
  d01_nlp_asoslari.*     |  NLP asoslari (PDF tayyor)
  d02_klassik_tasnif.tex |  Klassik tasnif (PDF hali yo'q — Overleaf kerak)
  d03_vektor_embedding.* |  Vektor embedding (PDF tayyor)
  d04_qidiruv_imlo.*     |  Qidiruv va imlo tuzatish (PDF tayyor)
  d05_til_modellari.*    |  N-grammalar, POS, HMM/Viterbi (PDF tayyor)
  d06_word2vec.*         |  Word2Vec / CBOW (PDF tayyor)
  d07_rnn.*              |  Rekurrent neyron tarmoqlar (PDF tayyor)
  d08_gru_lstm.*         |  GRU va LSTM (PDF tayyor)
  d09_matn_generatsiya.* |  Matn generatsiya, ikki tomonlama RNN (PDF tayyor)
  d10_ner.*              |  Nomlangan obyektlarni tanib olish (PDF tayyor)
  d11_seq2seq_attention.*|  Seq2Seq va Attention mexanizmi (PDF tayyor)

practices/               <- Amaliyot daftarlari (Kaggle Notebooks da ishlatiladi)
  d02_p1_preprocessing.*          Matn preprocessing
  d03_p2_sentiment.*              Sentiment tahlil
  d04_p3_embeddings.*             Embedding va qidiruv
  d05_p4_spell_lsh.*              Imlo tuzatish + LSH
  d06_p5_autocomplete_pos.*       Avtoto'ldirish + POS teglash
  d07_p6_word2vec.*               Word2Vec o'qitish
  d08_p7_rnn.*                    RNN tasniflovchi
  d09_p8_gru_lstm.*               GRU/LSTM taqqoslash
  d10_p9_textgen.*                Matn generatsiya (char-LSTM)
  d11_p10_ner.*                   NER (Bi-LSTM, IOB2)
  d12_p11_seq2seq.*               Seq2Seq tarjimon + Attention
  (har biri: tinglovchi varianti + _SOLUTIONS.ipynb javob kaliti)
  d02_checkpoints/ ... d12_checkpoints/   Offline ma'lumotlar

capstone/                <- Kapstone loyiha hujjatlari
  SPEC.md                  Loyiha shartnomasi va umumiy tavsif
  contracts.py             Barcha modullar uchun Python imzolari (type hints)
  modules/
    m01_text_preprocessor.py    1-kun  -- asosiy preprocessing
    m02_sentiment_classifier.py 3-kun  -- TF-IDF + Naive Bayes
    m03_pretrained_embedder.py  4-kun  -- tayyor embedding
    m04_spell_lsh_retriever.py  5-kun  -- imlo + LSH qidiruv
    m05_autocomplete.py         6-kun  -- N-gram avtoto'ldirish
    m05b_pos_tagger.py          6-kun  -- HMM POS teglash
    m06_custom_word2vec.py      7-kun  -- CBOW so'z vektorlari
    m07_rnn_classifier.py       8-kun  -- RNN sentiment
    m08_gru_lstm_classifier.py  9-kun  -- GRU/LSTM taqqoslash
    m09_text_generator.py      10-kun  -- char-LSTM generatsiya
    m10_ner_tagger.py          11-kun  -- Bi-LSTM NER
    m11_seq2seq_translator.py  12-kun  -- Seq2Seq + Bahdanau attention

milestones/              <- Haftalik milestone topshiriqlari
  w1_milestone.md / w1_check.py   1-hafta: m01-m02 integratsiyasi (muddat 22-iyun)
  w2_milestone.md / w2_check.py   2-hafta: m01-m05 integratsiyasi (muddat 29-iyun)
  w3_milestone.md / w3_check.py   3-hafta: m01-m08 taqqoslash    (muddat 6-iyul)

day1_orientation/        <- 1-kun: Orientatsiya
  d01_kirish.tex / .pdf    Orientatsiya slaydlari
  d01_orientatsiya.ipynb   Muhit tekshiruvi daftari (Kaggle da bajariladi)
  HISOB_YARATISH.md        Kaggle/HuggingFace/GitHub hisoblarini ochish yo'riqnomasi
  pre_course.docx / .xlsx  Oldindan ko'rib chiqish uchun materiallar

assessments/             <- Kurs oldi va kurs ichi baholash materiallari
```

---

## .tex fayllarni qanday kompilatsiya qilish (Overleaf)

1. **overleaf.com** -> *New Project -> Upload Project*
2. `.tex` faylini yuklang
3. *Recompile* tugmasini bosing (pdfLaTeX, ikki marta)
4. PDF yuklab olinadi

Barcha `.tex` fayllar o'z-o'ziga yetarli (tashqi `\input` yo'q).
Zarur paketlar: `beamer`, `tcolorbox`, `tikz`, `listings`, `booktabs`, `lmodern`
(Overleaf da barchasi mavjud).

---

## Amaliyot daftarlarini qanday ishlatish (Kaggle)

1. **kaggle.com** -> *Create Notebook -> File -> Import Notebook*
2. `.ipynb` faylini yuklang
3. *Run All* (`Shift+Enter` yoki *Run All*)
4. Birinchi katakda `OFFLINE_FALLBACK = True` — internet bo'lmasa ham ishlaydi

Har daftarning birinchi bo'limida zarur paketlar o'rnatiladi.

---

## Milestone o'z-o'zini tekshirish

Har bir hafta milestoni uchun `wN_check.py` skripti berilgan.
Tinglovchi uni ishga tushirib, o'z modullarini tekshirishi mumkin:

```
python milestones/w1_check.py   # 1-hafta (m01-m02)
python milestones/w2_check.py   # 2-hafta (m01-m05)
python milestones/w3_check.py   # 3-hafta (m01-m08)
```

---

## Eslatmalar ko'rib chiquvchiga

- **Tinglovchi varianti** va **javob kaliti** (`_SOLUTIONS`) har bir amaliyot uchun alohida berilgan.
- Daftarlardagi `assert` satrlari tinglovchining to'g'ri javob yozganini avtomatik tekshiradi.
- Kapstone loyiha har hafta bitta modul bilan to'ldirib boriladi; `capstone/modules/` papkasida
  hozircha m01-m11 modullar namuna sifatida berilgan (4-hafta modullari keyinroq).
- `course_map.yaml` — jadval, mavzular, o'lchanadigan maqsadlar va har kungi qo'lda
  hisoblangan namunaviy sonlar uchun yagona manba.
- `d02_klassik_tasnif.tex` uchun PDF hali kompilatsiya qilinmagan — Overleaf orqali olish mumkin.
