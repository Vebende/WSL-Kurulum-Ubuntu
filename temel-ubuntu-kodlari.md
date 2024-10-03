# WSL Üzerinde Temel Ubuntu Komutları

Ubuntu üzerinde WSL (Windows Subsystem for Linux) kullanırken temel komutlar şu şekilde sıralanabilir. Bunlar, günlük kullanımda en sık ihtiyaç duyulan komutlardır:

### Dosya ve Dizin Yönetimi

1. **`ls`**: Bulunduğunuz dizindeki dosya ve klasörleri listeler.
   ```bash
   ls -l  # Ayrıntılı listeleme yapar (izinler, boyut, tarih vs.)
   ls -a  # Gizli dosyaları da listeler
   ```

2. **`cd`**: Dizin değiştirmek için kullanılır.
   ```bash
   cd /home  # Belirtilen dizine gider
   cd ..     # Bir üst dizine gider
   cd ~      # Ana dizine gider
   ```

3. **`pwd`**: Bulunduğunuz dizinin tam yolunu gösterir.
   ```bash
   pwd
   ```

4. **`mkdir`**: Yeni bir dizin oluşturur.
   ```bash
   mkdir test  # "test" adında bir klasör oluşturur
   ```

5. **`rm`**: Dosya veya dizin silmek için kullanılır.
   ```bash
   rm file.txt    # Belirtilen dosyayı siler
   rm -r dir      # Dizin ve içindeki dosyaları siler
   ```

6. **`cp`**: Dosya veya dizin kopyalar.
   ```bash
   cp file.txt /path/to/destination  # Dosyayı belirtilen konuma kopyalar
   cp -r dir /path/to/destination    # Dizin ve içeriğini kopyalar
   ```

7. **`mv`**: Dosya veya dizin taşır veya adını değiştirir.
   ```bash
   mv old.txt new.txt                # Dosyanın adını değiştirir
   mv file.txt /path/to/destination  # Dosyayı belirtilen dizine taşır
   ```

### Dosya İçeriğini Görüntüleme

1. **`cat`**: Dosya içeriğini terminalde gösterir.
   ```bash
   cat file.txt  # Dosyanın içeriğini ekrana yazar
   ```

2. **`less`**: Büyük dosyaları sayfa sayfa incelemek için kullanılır.
   ```bash
   less file.txt  # Dosyanın içeriğini sayfa sayfa inceleyebilirsiniz
   ```

3. **`head` ve `tail`**: Dosyanın ilk veya son satırlarını gösterir.
   ```bash
   head file.txt  # Dosyanın ilk 10 satırını gösterir
   tail file.txt  # Dosyanın son 10 satırını gösterir
   ```

### Paket Yönetimi

1. **`sudo apt update`**: Paket listelerini günceller.
   ```bash
   sudo apt update
   ```

2. **`sudo apt upgrade`**: Yüklü paketleri günceller.
   ```bash
   sudo apt upgrade
   ```

3. **`sudo apt install <package-name>`**: Yeni bir paket yükler.
   ```bash
   sudo apt install git  # Git paketini yükler
   ```

4. **`sudo apt remove <package-name>`**: Paket kaldırır.
   ```bash
   sudo apt remove git  # Git paketini kaldırır
   ```

### Sistem Bilgileri ve Yönetimi

1. **`uname -r`**: Çekirdek (kernel) sürümünü gösterir.
   ```bash
   uname -r
   ```

2. **`df -h`**: Disk kullanımını gösterir.
   ```bash
   df -h
   ```

3. **`du -h`**: Belirtilen dizindeki dosya ve klasörlerin boyutlarını gösterir.
   ```bash
   du -h .  # Bulunduğunuz dizindeki dosya boyutlarını listeler
   ```

4. **`free -h`**: Bellek (RAM) kullanımını gösterir.
   ```bash
   free -h
   ```

5. **`top`**: Çalışan işlemleri ve sistem kaynaklarını gösterir.
   ```bash
   top
   ```

6. **`ps aux`**: Çalışan tüm süreçleri listeler.
   ```bash
   ps aux
   ```

7. **`kill`**: Süreçleri sonlandırır.
   ```bash
   kill <process-id>  # Belirtilen PID'ye sahip süreci sonlandırır
   ```

### Ağ ve Bağlantılar

1. **`ping`**: Belirtilen IP adresine veya siteye ping atar.
   ```bash
   ping google.com  # Google'a ping atar
   ```

2. **`ifconfig`**: Ağ arayüz bilgilerini gösterir.
   ```bash
   ifconfig
   ```

3. **`curl`**: HTTP istekleri yapmak için kullanılır.
   ```bash
   curl http://example.com  # URL'den veri çeker
   ```

4. **`wget`**: Bir URL'den dosya indirmek için kullanılır.
   ```bash
   wget http://example.com/file.zip  # URL'den dosya indirir
   ```

### Diğer Faydalı Komutlar

1. **`clear`**: Terminali temizler.
   ```bash
   clear
   ```

2. **`history`**: Girilen komutların geçmişini gösterir.
   ```bash
   history
   ```

3. **`man <command>`**: Bir komutun kullanım kılavuzunu gösterir.
   ```bash
   man ls  # 'ls' komutunun kullanım detaylarını gösterir
   ```
