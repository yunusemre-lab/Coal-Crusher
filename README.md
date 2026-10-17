# ⚙️ Coal Crusher Automation System with PLC & HMI

Siemens TIA Portal ortamında PLC (Ladder Diagram) ve SIMATIC HMI kullanılarak geliştirilmiş; kömür taşıma arabası hareketi, dolum süreçleri, kırıcı motor kontrolü ve modüler fonksiyon bloklarını içeren endüstriyel otomasyon projesidir.

---

## 📌 Proje Özeti
Bu proje, bir kömür kırma tesisindeki taşıma arabasının konumlandırılması, hammadde dolum operasyonları, sensör tabanlı güvenlik interlock'ları ve kırıcı sisteminin otomasyonunu kapsamaktadır. Sistem, manuel ve otomatik süreçleri optimize eden modüler bir mimariyle tasarlanmıştır.

### 🎥 HMI & Sistem Simülasyonu (PLC-Sim)

<img width="800" alt="Kömür Kırıcı HMI Simülasyonu" src="https://github.com/user-attachments/assets/35608845-0eab-4288-97d4-134122062ce3" />

---

## ⚙️ Özellikler ve Çalışma Mantığı

* **Araba Hareket Yönetimi (FB1):** Kömür taşıma arabasının ileri/geri yönlü hareketleri, sınır switch korumaları ve konum takibi modüler bloklar aracılığıyla yönetilir.
* **Dolum ve Kırma Operasyonları (FB2):** Kömür dolum bunkerlerinin kontrolü, seviye sensörleri, zamanlayıcılar ve kırıcı motorunun çalışma koşulları otomasyona bağlanmıştır.
* **Modüler Mimari:** Main (OB1) bloğu ana kontrol ve çağrıları üstlenirken; karmaşık mantıksal süreçler `FB1 (Araba)` ve `FB2 (Dolum)` fonksiyon blokları içinde izole edilmiştir.
* **Güvenlik ve Interlock:** Sensör geri beslemeleri ve acil durum durdurma koşulları ile sistem güvenliği sağlanmıştır.

---

## 🛠️ PLC Mimari ve Kod Yapısı

### 1. Ana Kontrol Blokları (Main OB1)

Sistemin temel tarama döngüsünü, ana başlatma/durdurma koşullarını ve blok çağrılarının yönlendirildiği ana program blokları:

![Main Network 1](https://github.com/user-attachments/assets/012f328b-b072-4cad-84e3-7ca0d660ecd2)
![Main Network 2](https://github.com/user-attachments/assets/d3fe8efb-dcfd-43e7-89eb-421461b014f1)
![Main Network 3](https://github.com/user-attachments/assets/b91e96b2-c2f1-4884-868b-6fea411b642e)
![Main Network 4](https://github.com/user-attachments/assets/9052886b-d947-4673-bc2b-0ae01c4811f3)
![Main Network 5](https://github.com/user-attachments/assets/b2b80286-e912-4da9-82a5-b05a1662edbc)

---

### 2. Modüler Fonksiyon Blokları (FB)

#### 🛒 FB1 (Araba): Taşıma Arabası Kontrol ve Konumlandırma Mantığı
Taşıma arabasının hareket senaryolarını, yön komutlarını ve konum algoritmalarını içeren ağ yapısı:

![FB1 Network 1](https://github.com/user-attachments/assets/e864d29c-2af3-46c8-8446-1f75dbda8260)
![FB1 Network 2](https://github.com/user-attachments/assets/eabb7cc8-69fb-4c76-8550-f0d23e301aad)
![FB1 Network 3](https://github.com/user-attachments/assets/115399b3-8830-46f3-bc13-4aed6f7fced1)

---

#### 🏭 FB2 (Dolum): Malzeme Dolum ve Kırıcı Süreç Yönetimi
Dolum kapakları, seviye kontrolleri, zamanlayıcılar ve kırıcı aktivasyon mantığını yöneten detaylı fonksiyon blok ağları:

![FB2 Network 1](https://github.com/user-attachments/assets/e2cd4288-844b-4268-ae97-79fedae9421c)
![FB2 Network 2](https://github.com/user-attachments/assets/6ebd5de7-e971-4948-be9c-713e3bc63e66)
![FB2 Network 3](https://github.com/user-attachments/assets/f395cbb2-d8b0-4c1c-9301-43c024c73576)
![FB2 Network 4](https://github.com/user-attachments/assets/317b8016-ed90-4948-b29b-04e3e9482476)
![FB2 Network 5](https://github.com/user-attachments/assets/bc59f20e-6a06-42a5-b928-3111fcb431e4)
![FB2 Network 6](https://github.com/user-attachments/assets/f7bf8f17-3ba4-4c0a-95d4-df0c043444d8)
![FB2 Network 7](https://github.com/user-attachments/assets/9900ed75-9d44-4da3-8b9a-b655068a3fd7)
![FB2 Network 8](https://github.com/user-attachments/assets/bbe7be69-3976-4341-80c8-bfb5b5bd1a94)

---

## 🛠️ Kullanılan Teknolojiler

* **Yazılım:** Siemens TIA Portal
* **Programlama Dili:** Ladder Diagram (LAD)
* **Arayüz (HMI):** SIMATIC HMI Touch Panel Simulation
* **Simülasyon:** S7-PLCSIM
