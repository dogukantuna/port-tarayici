# 🔍 Mini Port Scanner

Python ile yazılmış çok iş parçacıklı (multi-threaded) bir TCP/UDP port tarayıcı. Servisleri, versiyonları ve banner verilerini tespit eder. Aynı zamanda tarama çıktısını log dosyasına kaydeder.

## 🚀 Özellikler

- ✅ TCP port tarama
- ✅ UDP port tarama
- ✅ Banner grabbing (servislerden veri çekme)
- ✅ Servis adı tespiti (FTP, SSH, HTTP vs.)
- ✅ Versiyon tanıma (Apache 2.4.41, OpenSSH 7.4 vs.)
- ✅ Loglama (çıktılar `logs/tarama_sonuc.txt` dosyasına yazılır)
- ✅ Çoklu iş parçacığı ile hızlı tarama

## 🧰 Gereksinimler

```bash
pip install -r requirements.txt
```

## ⚙️ Kullanım

```bash
python scanner.py -t <hedef_ip> -p <port_aralığı> [--udp]
```

### Örnekler:

```bash
python scanner.py -t 192.168.1.1 -p 20-100
python scanner.py -t 192.168.1.1 -p 1-1024 --udp
```

## 📁 Log Dosyası

Tüm tarama sonuçları `logs/tarama_sonuc.txt` dosyasına yazılır.  
Her taramanın sonunda otomatik olarak imzalanır:

```
Coded by Doğukan Tuna
```

## 📌 Not

Bu proje eğitim amaçlıdır. İzinsiz ağlara tarama yapmanız yasal sonuçlar doğurabilir.
