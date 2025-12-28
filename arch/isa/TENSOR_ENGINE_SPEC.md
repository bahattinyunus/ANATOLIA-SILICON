# 🧠 Anatolia Tensor Engine (ATE) - Gen 1 Micro-Architecture Specification

ATE, yüksek yoğunluklu matris operasyonları için özelleştirilmiş, ölçeklenebilir bir hesaplama ünitesidir.

## 📐 Mimari Parametreler
- **Matris Boyutu:** 16x16 (Native Tile Size).
- **Data Flow:** Weight-Stationary (Ağırlık-Sabit) veri akışı.
- **SRAM Buffer:** 2MB Local Scratchpad (L0).

## 🚀 Pipeline Yapısı
ATE, 5 aşamalı özel bir tensör pipeline'ı kullanır:
1. **Fetch/Dispatch:** Komutların vektör registerlarından çekilmesi.
2. **Operand Alignment:** Verilerin matris çarpım birimine hizalanması.
3. **Matrix MAC Units:** 256 paralel çarpan-toplayıcı ünitesi.
4. **Post-Processing:** Aktivasyon (ReLU/GELU) ve Quantization.
5. **Commit:** Sonuçların HBM veya L2 önbelleğe yazılması.

## 🔋 Güç Tasarımı
Düşük voltajda (0.7V) çalışma ve dinamik "Gated-Clock" teknolojisi ile rakiplerine göre %30 daha az sızıntı (leakage) akımı.
