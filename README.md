# fortigate-web-filtering-lab1
Web filtering configuration using FortiGate firewall in a local network environment

Bu projede, oluşturduğum bir local ağ(LAN) ortamında güvenli internet erişimi sağlamak ve belirli web sitelerine eişimi engellemek amacıyla Fortinet'in güvenlik duvarı cihazı FortiGate kullanrak web filtreleme yapılandırması gerçekleştirilmiştir.

🖥️ Lab Ortamı
1x FortiGate Firewall
1x Server PC
1x Client PC
Local Area Network (LAN)
WAN üzerinden internet çıkışı
Tüm LAN trafiği FortiGate üzerinden internete yönlendirilmiştir.

⚙️ Yapılandırma
-LAN ve WAN interface ayarları
    -LAN ağımız 10.10.10.0/24 Ipv4 ağıyla oluşturduk WAN ağımız ise moderme bağlı olan portumuz onun Ipv4 adresi (192.168.1.126) modermden static olarak verdim.
    <img width="855" height="627" alt="1" src="https://github.com/user-attachments/assets/45c4c42f-2218-42d8-b6d8-11b5d18ae42e" /><img width="1106" height="795" alt="2" src="https://github.com/user-attachments/assets/52412fe8-de7f-4962-bb27-c48359b4196c" />
   - static router 0.0.0.0/0 olarak ayarladım, neden LAN istemcilerin internete erişebilmesi için.Bu rota routing tablosunda eşleşmeyen tüm trafik için internet çıkışı sağlar
     <img width="885" height="528" alt="5" src="https://github.com/user-attachments/assets/c47696f1-63e0-4f1e-95cd-c543c1893958" />
   -Aşağdaki görsel, LAN’dan WAN’a giden trafik için FortiGate üzerinde tanımlanan firewall policy’yi göstermektedir.
    <img width="866" height="710" alt="3" src="https://github.com/user-attachments/assets/855f0afb-bf1a-4c44-bbf9-a6226dcb2428" />
-NAT ayarları
-Web filtre profile tanımlama
-URL ve kategori bazlı web siteleri engelleme

🔐 Güvenlik Senaryosu

Oluşturulan web filtre politikaları sayesinde:
Belirlenen web sitelerine erişim engellenmiştir
İstenmeyen içerik kategorileri bloklanmıştır
İnternet erişimi firewall üzerinden kontrol altına alınmıştır

✅ Test Sonuçları
Engellenen sitelere erişim denemelerinde erişim sağlanamamıştır
Firewall logları üzerinden trafik başarıyla izlenmiştir
Güvenli internet çıkışı doğrulanmıştır
<img width="1717" height="868" alt="6" src="https://github.com/user-attachments/assets/f3a3bd7d-10a9-4111-b49c-76cc6e07e1b8" />
<img width="636" height="270" alt="FortiProje" src="https://github.com/user-attachments/assets/5fa3f751-a017-41e9-a8ef-beb2ebe3d4a7" />

