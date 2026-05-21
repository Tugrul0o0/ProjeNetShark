# 🦈 NetShark — Canlı Ağ Güvenliği & DDoS Tehdit Simülatörü
NetShark, ağ trafiğini gerçek zamanlı olarak izleyen, siber tehditleri (özellikle DDoS saldırılarını) tespit eden ve bunlara karşı aktif savunma mekanizmaları (IP Engelleme, Hız Sınırlama, Acil Durum Modu vb.) simüle eden fütüristik, siber operasyon merkezi (SOC) tarzında tasarlanmış bir **Ağ Güvenlik Paneli** simülasyonudur.
---
## 📸 Ekran Görüntüleri (Screenshots)

| 📊 Gösterge Paneli (Dashboard) | 🚨 Canlı Tehdit Algılama |
| :--- | :--- |
| <img src="https://via.placeholder.com/400x220/0f1520/c8d8f0?text=NetShark+Dashboard" width="100%" alt="Dashboard"/> | <img src="https://via.placeholder.com/400x220/141c2e/ff3d5a?text=Threat+Detection" width="100%" alt="Threats"/> |

*Not: Kendi ekran görüntülerinizi aldığınızda yukarıdaki `https://via.placeholder.com/...` linklerini projenizin içindeki görsel yolları ile değiştirebilirsiniz.*
---
## ✨ Öne Çıkan Özellikler
* **📈 Canlı Grafik Entegrasyonu:** `Chart.js` ile güçlendirilmiş; Gelen (GEL), Giden (GİD) ve Engellenen (BLK) trafiği anlık olarak çizen çizgi grafik.
* **🚨 Gelişmiş Tehdit Simülatörü:** Tek tıkla başlatılabilen 6 farklı popüler siber saldırı türü:
    * 🌊 **SYN Flood** (TCP el sıkışması suistimali)
    * 📡 **UDP Flood** (Bant genişliği tüketimi)
    * 🔁 **HTTP GET Flood** (Uygulama katmanı bot saldırısı)
    * 🐌 **Slowloris** (Yavaş başlık akışı ile bağlantı havuzu tüketimi)
    * 📶 **ICMP Ping Flood** (CPU ve gecikme manipülasyonu)
    * 📣 **DNS Amplifikasyon** (Yüksek hacimli yansıtma saldırısı)
* **🛠 Aktif Savunma Eylemleri (Mitigation):** Tehditlere karşı dinamik tepki verme:
    * 🚫 Şüpheli IP'leri tek tıkla veya otomatik kara listeye (Blacklist) alma.
    * ⏱ **Rate Limiting** (Hız sınırlama) ile gelen trafiği %40 oranında baskılama.
    * 🌍 Coğrafi filtreleme ve 🔍 Derin Paket İncelemesi (DPI) modları.
    * 🆘 **Acil Durum Modu (Emergency):** Sadece güvenli listeye izin vererek sistemi koruma.
* **🔍 Derinlemesine Paket İnceleme (DPI):** Yakalanan paketlerin TTL, Kontrol Toplamı (Checksum), Pencere Boyutu, Kaynak Ülke, ISP ve HTTP User-Agent detaylarını anlık görebilme.
* **📜 Canlı Olay Günlüğü (Log):** Gerçek zamanlı akan renk kodlu siber olay log akışı.
---
## 🛠 Kullanılan Teknolojiler
* **Dil:** Pure JavaScript (ES6+), HTML5, CSS3
* **Tasarım Konsepti:** Cyberpunk / Dark SOC (Siber Operasyon Merkezi) Arayüzü
* **Tipografi:** `JetBrains Mono` (Fütüristik Geliştirici Yazı Tipi)
* **Kütüphaneler:** [Chart.js v4.4.1](https://www.chartjs.org/) (Grafik işleme için CDN üzerinden entegre edilmiştir)
---
## 🚀 Kurulum ve Çalıştırma
Proje tamamen istemci taraflı (Client-side) çalıştığı için herhangi bir sunucu kurulumuna veya `npm install` bağımlılığına **ihtiyaç duymaz**.
1.  Bu depoyu bilgisayarınıza indirin veya klonlayın:
    ```bash
    git clone [https://github.com/Tugrul0o0/ProjeNetShark.git](https://github.com/Tugrul0o0/ProjeNetShark.git)
    ```
2.  Proje klasörünün içindeki ana HTML dosyasını (örneğin `index.html`) tarayıcınızda çift tıklayarak açın.
3.  **Simülatör** sekmesine gidip bir saldırı türünü başlatarak ağ panelinin tepkilerini canlı olarak izleyin!
---
## 🛡 Algoritma ve Trafik Mantığı
Panel arkada saniyede bir tetiklenen bir `tick()` döngüsüne sahiptir. Aktif ettiğiniz simülasyonlara ve uyguladığınız güvenlik kurallarına göre grafik verileri matematiksel olarak dinamik şekilde manipüle edilir:
* **Saldırı Başlatıldığında:** Gelen trafik (Mbps) ve aktif IP bağlantı sayıları saldırının kritiklik seviyesine göre katlanarak artar.
* **Güvenlik Kuralları Açıldığında:** Grafik anlık olarak engellenen paketleri (BLK) listeler ve gelen zararlı trafiği süzerek normal seviyelere çekmeye çalışır.
---
## 📝 Lisans
Bu proje eğitim ve siber güvenlik farkındalığı amacıyla geliştirilmiştir. İstediğiniz gibi geliştirebilir, çatallayabilir (fork) ve projelerinizde kullanabilirsiniz. 
---
💡 *Geliştirici Notu: NetShark arayüzü tamamen responsive olup, terminal estetiği göz önünde bulundurularak tasarlanmıştır.*
