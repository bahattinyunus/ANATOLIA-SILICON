# ⚙️ Anatolia Vector (AS-V) ISA Specification v0.1

Anatolia Vector (AS-V), RISC-V tabanlı ancak yapay zeka operasyonları için radikal olarak genişletilmiş bir komut seti mimarisidir. Bu döküman, NVIDIA CUDA çekirdeklerine karşı asimetrik üstünlük sağlayan vektör operasyonlarını tanımlar.

## 📐 Tasarım İlkeleri
1. **Maksimum Vektör Uzunluğu (VLEN):** 2048-bit (Standart RISC-V'den daha geniş).
2. **Matris Yerel Operasyonlar:** Tensör hesaplamaları için doğrudan vektör-matris komutları.
3. **Esnek Veri Tipleri:** FP8, NF4 ve BF16 için donanımsal optimizasyon.

## 🧩 Özel Komut Setleri (Anatolia Extensions)

### 1. MatrixMultiply-Accumulate (MMA)
`as.mma.v <vd>, <vs1>, <vs2>`
- **İşlev:** `vd = vd + (vs1 * vs2)` (Vektör matris çarpımı).
- **Verim:** Tek bir saat vuruşunda 256 matris elemanını işleme kapasitesi.

### 2. Nonlinear Activation (ACT)
`as.act.relu <vd>, <vs1>`
`as.act.gelu <vd>, <vs1>`
- **İşlev:** Vektör üzerindeki elemanlara doğrudan aktivasyon fonksiyonu uygular.
- **Donanımsal Hızlandırma:** Look-up table (LUT) yerine doğrudan matematiksel çekirdekler kullanılır.

### 3. Quantization Aware Load (QAL)
`as.qal.load.nf4 <vd>, (<rs1>)`
- **İşlev:** Bellekten NF4 (NormalFloat4) verisini okur ve anında BF16 formatına dequantize ederek vektör register'larına yükler.

---

## 🗄️ Register Dosyası Yapısı
- **32 Adet Vektör Register (v0-v31):** Her biri 2048-bit genişliğinde.
- **8 Adet Mask Register (m0-m7):** Koşullu operasyonlar için.

## 🚀 Performans Hedefleri
Anatolia Silicon AS-V Core, standart bir RISC-V vektör ünitesinden 4 kat, NVIDIA Tensor çekirdeklerinden ise matris başına %30 daha az enerji tüketerek aynı verimi hedeflemektedir.
