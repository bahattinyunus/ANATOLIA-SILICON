# 🚀 Anatolia Silicon'a Giriş: İlk Adımlar

Hoş geldiniz! Bu rehber, Anatolia Silicon ekosistemine yeni katılan mühendisler ve araştırmacılar için tasarlanmıştır.

## 🛠️ Kurulum ve Gereksinimler
Proje hem donanım simülasyonu hem de yazılım katmanlarını içerir.

### 1. Simülasyon Ortamı
RTL tasarımlarını denemek için şunlara ihtiyacınız olacak:
- **Verilator** veya **Icarus Verilog** (Açık kaynak simülatörler).
- **Python 3.10+** (ATE simülasyonu için).

### 2. Derleyici Katmanı (ACS)
- **LLVM 16+** (ACS backend geliştirmeleri için).

## 📂 Depo Yapısını Tanıyın
- `arch/`: Mimari spesifikasyonlar.
- `src/rtl/`: Gerçek donanım tasarımları.
- `src/lib/`: Python tabanlı hızlı prototipleme araçları.
- `sim/`: Test ve doğrulama ortamları.

## 🧪 İlk Simülasyonu Çalıştırın
Basit matris çarpım motorunu test etmek için:
```bash
python src/lib/ate_sim.py
```

Anadolu'nun zekası parmaklarınızın ucunda.
