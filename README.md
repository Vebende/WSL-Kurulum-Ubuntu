### 1. **Windows 10 veya 11 Sürüm Kontrolü**
   - **Windows 10**: En az 1903 (Build 18362) veya daha yeni bir sürüm gereklidir.
   - **Windows 11**: WSL varsayılan olarak desteklenmektedir.
   - Windows sürümünüzü kontrol etmek için `Win + R` tuşlarına basarak **`winver`** komutunu çalıştırabilirsiniz.

### 2. **WSL Özelliğini Aktifleştirme**
   WSL, Windows’ta varsayılan olarak kapalıdır ve elle aktifleştirilmesi gerekir.

#### Yöntem 1: PowerShell ile Aktifleştirme (Tavsiye Edilen Yöntem)
   1. **PowerShell’i Yönetici Olarak Açın**:
      - Başlat menüsünden **PowerShell** aratarak sağ tıklayın ve "Yönetici olarak çalıştır" seçeneğini seçin.
   
   2. **WSL ve Sanallaştırma Özelliğini Etkinleştirin**:
      Aşağıdaki komutu PowerShell penceresine yazın:
      ```bash
      wsl --install
      ```
      Bu komut, hem WSL 1 hem de WSL 2 desteğini etkinleştirir ve gerekli bileşenleri kurar (Linux çekirdeği dahil).

#### Yöntem 2: Denetim Masası ile Etkinleştirme
   1. **Denetim Masası'nı Açın**:
      - Başlat menüsünde **Denetim Masası** arayın ve açın.
   
   2. **Programlar ve Özellikler'e Gidin**:
      - "Programlar" bölümünün altında **Windows Özelliklerini Aç veya Kapat** seçeneğine tıklayın.
   
   3. **WSL'i Etkinleştirin**:
      - Listeden **Windows Subsystem for Linux** ve **Virtual Machine Platform** kutucuklarını işaretleyin ve **Tamam** butonuna tıklayın.

   4. Bilgisayarı yeniden başlatın.

### 3. **WSL 2 için Ek Adımlar (Gerekliyse)**
   WSL 2, daha iyi performans ve tam Linux çekirdeği desteği sağlar. WSL 2'yi kullanmak için aşağıdaki ek adımları izleyin:

   1. **Sanal Makine Platformu'nu Etkinleştirin**:
      Aşağıdaki komutu yönetici haklarına sahip PowerShell'de çalıştırın:
      ```bash
      dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
      ```

   2. **Linux Çekirdeğini Güncelleyin**:
      - Microsoft’un resmi web sitesinden **Linux çekirdeği güncellemesi**ni indirip yüklemeniz gerekebilir: [WSL 2 Linux çekirdek güncellemesi](https://aka.ms/wsl2kernel).

   3. **WSL Varsayılan Versiyonunu Ayarlayın**:
      PowerShell’e şu komutu girin:
      ```bash
      wsl --set-default-version 2
      ```

### 4. **İşlemci Sanallaştırmasını Etkinleştirme**
   WSL 2'nin çalışabilmesi için BIOS/UEFI ayarlarında **donanım sanallaştırmasının (virtualization)** etkinleştirilmiş olması gerekir.

   1. Bilgisayarınızı yeniden başlatın ve BIOS/UEFI ayarlarına girin.
   2. **Intel VT-x** (Intel işlemciler için) veya **AMD-V** (AMD işlemciler için) seçeneklerini bulun ve etkinleştirin.

### 5. **Linux Dağıtımını Yükleme**
   WSL kurulumunu tamamladıktan sonra, tercih ettiğiniz Linux dağıtımını Windows Mağaza'dan (Microsoft Store) yükleyebilirsiniz:

   1. **Microsoft Store**'u açın.
   2. "Ubuntu", "Debian", "Kali Linux", "openSUSE" gibi tercih ettiğiniz bir dağıtımı aratın ve yükleyin.
   3. Yükledikten sonra, Başlat menüsünden dağıtımınıza tıklayarak terminali başlatın ve kurulum adımlarını takip edin (kullanıcı adı ve şifre belirleme gibi).

### 6. **WSL Ayarlarını Yönetmek**
   - Yüklü Linux dağıtımlarını görmek için şu komutu kullanabilirsiniz:
     ```bash
     wsl -l -v
     ```
   - Varsayılan WSL sürümünü değiştirmek veya dağıtımlar arasında geçiş yapmak için:
     ```bash
     wsl --set-version <distribution-name> 2
     ```
# WSL Üzerine Ubuntu Kurulumu

WSL üzerinde online Linux dağıtımlarını listelemek ve Ubuntu'yu kurmak için şu adımları takip edebilirsiniz:

### 1. **Mevcut Linux Dağıtımlarını Listeleme**
   PowerShell veya komut istemcisi (CMD) üzerinden mevcut Linux dağıtımlarını görmek için aşağıdaki komutu çalıştırın:
   ```bash
   wsl --list --online
   ```
   Bu komut, Microsoft Store'da WSL için mevcut olan tüm Linux dağıtımlarını listeler.

### 2. **Ubuntu'yu Kurma**
   Ubuntu'yu yüklemek için, listedeki **Ubuntu** dağıtımını seçip aşağıdaki komutu çalıştırın:
   ```bash
   wsl --install -d Ubuntu
   ```
   Bu komut, Ubuntu'yu indirip kurar ve varsayılan Linux dağıtımı olarak ayarlar.

### 3. **Ubuntu Kurulumu Tamamlandığında**
   Kurulum tamamlandıktan sonra, Ubuntu terminalini başlatmak için şu komutu kullanabilirsiniz:
   ```bash
   wsl
   ```
   Terminal ilk başlatıldığında, kullanıcı adı ve parola gibi temel ayarları yapmanız istenecektir.

### 4. **Kurulu Dağıtımları Görüntüleme**
   WSL üzerinde kurulu tüm Linux dağıtımlarını görmek için şu komutu çalıştırabilirsiniz:
   ```bash
   wsl -l -v
   ```
   Bu komut, yüklü dağıtımların adını ve WSL sürümünü (1 veya 2) gösterir.

Bu adımları takip ederek WSL üzerinde Ubuntu dağıtımını sorunsuz bir şekilde kurabilirsiniz.
