# 🌊 Anatolia Memory & Interconnect Hierarchy

GPU performansındaki en büyük tıkanıklık "Bellek Duvarı" (Memory Wall) sorunudur. Anatolia Silicon, bu duvarı devasa bant genişliği ve ışık tabanlı iletişim ile yıkar.

## 💎 HBM3e & HBM4 Entegrasyonu
Anatolia Silicon (AS-1), silikon üzerine doğrudan 3D paketleme (CoWoS) ile entegre edilmiş HBM3e katmanlarını kullanır.
- **Bant Genişliği:** 8 TB/s (AS-1 Max).
- **Kapasite:** Her GPU birimi için 192GB veya 288GB opsiyonları.
- **Latency:** Bellek kontrolcüleri, AS-V çekirdeklerine doğrudan (direct-to-core) bağlıdır; ara katman gecikmeleri elimine edilmiştir.

## 💡 Anatolia Photonix Interconnect (API)
Bakır kabloların elektriksel limitleri (R-C gecikmeleri) aşılmak zorundadır. Anatolia Silicon, çipler arası ve raflar arası iletişimde fotonları kullanır.

### Teknolojik Avantajlar:
1. **Sıfır Direnç:** Işık sinyalleri ısı yaymaz, bu da soğutma maliyetlerini %40 düşürür.
2. **Infinite Scale:** 10,240 GPU çekirdeğini tek bir "Virtual Unified Supercomputer" olarak bağlama kapasitesi.
3. **Hız:** 400 Gbps hattı üzerinden 1.6 Tbps'ye kadar ölçeklenebilir optik bağlantı.

## 🏗️ Bellek Hiyerarşisi (Top-Down)
1. **L0 (Private Cache):** 64KB, her AS-V Core için.
2. **L1 (Shared SRAM):** 4MB, her Chiplet için.
3. **L2 (Global Scratchpad):** 96MB, yüksek hızlı SRAM.
4. **L3 (HBM3e Stack):** Ana yüksek kapasiteli bellek.
5. **Remote (Photonix):** Diğer GPU'ların belleklerine doğrudan erişim.

---
Anadolu'nun zekası, ışık hızıyla harmanlanıyor.
