# 🌊 Anatolia Cache Coherence Protocol: H-SYNC (Hybrid Sync)

Anatolia Silicon, binlerce çekirdek arasında veri tutarlılığını sağlamak için geleneksel MESI protokolünün ötesinde, fotonik tabanlı bir hibrid protokol kullanır.

## 🛡️ H-SYNC İlkeleri
1. **Optical Snooping:** Çipler arası tutarlılık sinyalleri bakır yollar yerine Photonix hatları üzerinden ışık hızıyla yayılır.
2. **Directory-Based Scaling:** Binlerce chiplet için merkezi olmayan, dağıtık dizin (directory) yapısı.
3. **Zero-Wait Invalidation:** Write-back operasyonlarında geçersiz kılma sinyalleri nano-saniye mertebesinde tüm kümeye iletilir.

## 📊 Durum Tanımları
- **M (Modified):** Veri sadece bu çekirdekte ve değiştirilmiş.
- **S (Shared):** Veri birden fazla çekirdekte aynı.
- **I (Invalid):** Veri güncelliğini yitirmiş.
- **A (Anatolian-Global):** Veri fotonik olarak tüm küme için rezerve edilmiş.
