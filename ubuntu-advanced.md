# İşletim Sistemi Bilgilerinin Alınması
```bash
sudo cat /etc/os-release
```


Aşağıda verdiğiniz Ubuntu bilgilerini Markdown formatında düzenledim:

```markdown
# Ubuntu Bilgileri

- **Pretty Name**: Ubuntu 22.04.1 LTS
- **Name**: Ubuntu
- **Version ID**: 22.04
- **Version**: 22.04.1 LTS (Jammy Jellyfish)
- **Version Codename**: jammy
- **ID**: ubuntu
- **ID Like**: debian
- **Home URL**: [https://www.ubuntu.com/](https://www.ubuntu.com/)
- **Support URL**: [https://help.ubuntu.com/](https://help.ubuntu.com/)
- **Bug Report URL**: [https://bugs.launchpad.net/ubuntu/](https://bugs.launchpad.net/ubuntu/)
- **Privacy Policy URL**: [https://www.ubuntu.com/legal/terms-and-policies/privacy-policy](https://www.ubuntu.com/legal/terms-and-policies/privacy-policy)
- **Ubuntu Codename**: jammy
```

## CPU bilgilerinin alınması
```bash
sudo cat /proc/cpuinfo
```

```markdown
# CPU Bilgileri

## Processor 0
- **Vendor ID**: GenuineIntel
- **CPU Family**: 6
- **Model**: 62
- **Model Name**: Intel(R) Xeon(R) CPU E5-2697 v2 @ 2.70GHz
- **Stepping**: 4
- **Microcode**: 0xffffffff
- **CPU MHz**: 2693.508
- **Cache Size**: 30720 KB
- **Physical ID**: 0
- **Siblings**: 48
- **Core ID**: 0
- **CPU Cores**: 24
- **APIC ID**: 0
- **Initial APIC ID**: 0
- **FPU**: Yes
- **FPU Exception**: Yes
- **CPUID Level**: 13
- **WP**: Yes
- **Flags**: fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc arch_perfmon rep_good nopl xtopology cpuid pni pclmulqdq ssse3 cx16 pdcm pcid sse4_1 sse4_2 popcnt aes xsave avx f16c rdrand hypervisor lahf_lm pti ssbd ibrs ibpb stibp fsgsbase smep erms xsaveopt md_clear flush_l1d arch_capabilities
- **Bugs**: cpu_meltdown spectre_v1 spectre_v2 spec_store_bypass l1tf mds swapgs itlb_multihit mmio_unknown
- **Bogomips**: 5387.01
- **Clflush Size**: 64
- **Cache Alignment**: 64
- **Address Sizes**: 46 bits physical, 48 bits virtual
- **Power Management**:

## Processor 1
- **Vendor ID**: GenuineIntel
- **CPU Family**: 6
- **Model**: 62
- **Model Name**: Intel(R) Xeon(R) CPU E5-2697 v2 @ 2.70GHz
- **Stepping**: 4
- **Microcode**: 0xffffffff
- **CPU MHz**: 2693.508
- **Cache Size**: 30720 KB
- **Physical ID**: 0
- **Siblings**: 48
- **Core ID**: 0
- **CPU Cores**: 24
- **APIC ID**: 1
- **Initial APIC ID**: 1
- **FPU**: Yes
- **FPU Exception**: Yes
- **CPUID Level**: 13
- **WP**: Yes
- **Flags**: fpu vme de pse tsc msr pae mce cx8 apic sep mtrr pge mca cmov pat pse36 clflush mmx fxsr sse sse2 ss ht syscall nx pdpe1gb rdtscp lm constant_tsc arch_perfmon rep_good nopl xtopology cpuid pni pclmulqdq ssse3 cx16 pdcm pcid sse4_1 sse4_2 popcnt aes xsave avx f16c rdrand hypervisor lahf_lm pti ssbd ibrs ibpb stibp fsgsbase smep erms xsaveopt md_clear flush_l1d arch_capabilities
- **Bugs**: cpu_meltdown spectre_v1 spectre_v2 spec_store_bypass l1tf mds swapgs itlb_multihit mmio_unknown
- **Bogomips**: 5387.01
- **Clflush Size**: 64
- **Cache Alignment**: 64
- **Address Sizes**: 46 bits physical, 48 bits virtual
- **Power Management**:
```


# Ubuntu Disk Bilgileri

Aşağıdaki komutlar, Ubuntu sisteminizde disk bilgilerini görüntülemenize yardımcı olur.

## 1. Disk Alanını Görüntüleme

Disk alanı kullanımını görüntülemek için `df` komutunu kullanabilirsiniz:

```bash
df -h
```
- `-h`: İnsan tarafından okunabilir biçimde çıktı verir.

## 2. Disklerin ve Bölümlerinin Listesini Görüntüleme

Tüm diskleri ve bölümlerini listelemek için `lsblk` komutunu kullanabilirsiniz:

```bash
lsblk
```

## 3. Disklerin Detaylı Bilgilerini Görüntüleme

Diskler hakkında daha ayrıntılı bilgi almak için `fdisk` komutunu kullanabilirsiniz:

```bash
sudo fdisk -l
```

## 4. Disk Kullanımını Görüntüleme

Disk kullanımıyla ilgili daha ayrıntılı bilgi almak için `du` komutunu kullanabilirsiniz:

```bash
du -sh *
```
- `-s`: Toplam boyutu gösterir.
- `-h`: İnsan tarafından okunabilir biçimde çıktı verir.

## 5. Disk Sağlığını Kontrol Etme

Diskin sağlık durumunu kontrol etmek için `smartctl` komutunu kullanabilirsiniz (öncelikle `smartmontools` paketinin yüklü olması gerekir):

```bash
sudo smartctl -a /dev/sda
```

Yukarıdaki komutlarda `/dev/sda` kısmını sisteminizdeki diskin adıyla değiştirmeyi unutmayın.


Ubuntu'da CPU bilgilerini görüntülemek için kullanılabilecek bazı komutlar ve bunların açıklamalarıyla birlikte Markdown formatında bir belge hazırladım:

# Ubuntu CPU Bilgileri

Aşağıdaki komutlar, Ubuntu sisteminizde CPU bilgilerini görüntülemenize yardımcı olur.

## 1. CPU Bilgilerini Görüntüleme

CPU ile ilgili temel bilgileri görüntülemek için `lscpu` komutunu kullanabilirsiniz:

```bash
lscpu
```

## 2. /proc CPU Bilgileri

CPU hakkında daha fazla bilgi almak için `/proc/cpuinfo` dosyasını görüntüleyebilirsiniz:

```bash
cat /proc/cpuinfo
```

## 3. CPU Kullanımını Görüntüleme

CPU kullanımını gerçek zamanlı olarak izlemek için `top` veya `htop` komutlarını kullanabilirsiniz:

```bash
top
```

veya

```bash
htop
```
> **Not**: `htop` kullanmak için öncelikle `htop` paketini yüklemeniz gerekebilir:

```bash
sudo apt install htop
```

## 4. CPU Hızı ve Yükü Görüntüleme

CPU hızını ve yükünü görüntülemek için `mpstat` komutunu kullanabilirsiniz. `sysstat` paketini yüklemeniz gerekebilir:

```bash
sudo apt install sysstat
```

Ardından şu komutu çalıştırabilirsiniz:

```bash
mpstat
```

## 5. CPU Isısı ve Sağlığını Kontrol Etme

CPU sıcaklığını kontrol etmek için `sensors` komutunu kullanabilirsiniz. `lm-sensors` paketini yüklemeniz gerekebilir:

```bash
sudo apt install lm-sensors
```

Ardından aşağıdaki komutu çalıştırın:

```bash
sensors
```

# Ubuntu Ağ Bilgileri

Aşağıdaki komutlar, Ubuntu sisteminizde ağ bilgilerini görüntülemenize ve yönetmenize yardımcı olur.

## 1. Ağ Bağlantılarını Görüntüleme

Ağ arayüzleri ve bağlantı durumunu görüntülemek için `ip` komutunu kullanabilirsiniz:

```bash
ip addr show
```

veya daha basit bir şekilde:

```bash
ifconfig
```
> **Not**: `ifconfig` komutu, modern sistemlerde genellikle yüklü değildir. `net-tools` paketini yüklemeniz gerekebilir:

```bash
sudo apt install net-tools
```

## 2. Aktif Ağ Bağlantılarını Görüntüleme

Aktif ağ bağlantılarını ve dinleme durumundaki portları görmek için `netstat` veya `ss` komutunu kullanabilirsiniz:

```bash
netstat -tuln
```

veya

```bash
ss -tuln
```

## 3. Ağ Geçidini ve DNS Ayarlarını Görüntüleme

Ağ geçidi ve DNS ayarlarını görüntülemek için:

```bash
cat /etc/resolv.conf
```

veya ağ yapılandırma dosyalarını kontrol edebilirsiniz:

```bash
cat /etc/network/interfaces
```

## 4. Ağ Durumunu Kontrol Etme

Ağ bağlantısının durumunu kontrol etmek için `ping` komutunu kullanabilirsiniz:

```bash
ping google.com
```

## 5. Ağ Arayüzünü Yenileme

Bir ağ arayüzünü yeniden başlatmak için aşağıdaki komutları kullanabilirsiniz:

```bash
sudo ip link set <interface> down
sudo ip link set <interface> up
```
> `<interface>` kısmını, örneğin `eth0` veya `wlan0` gibi uygun ağ arayüzü adıyla değiştirin.

## 6. Ağ Bağlantısını Test Etme

Bir ağ bağlantısını test etmek için `traceroute` komutunu kullanabilirsiniz. Öncelikle `traceroute` paketini yüklemeniz gerekebilir:

```bash
sudo apt install traceroute
```

Ardından şu komutu çalıştırın:

```bash
traceroute google.com
```

# Ubuntu Port Yönlendirme

Aşağıdaki adımlar, Ubuntu sisteminizde port yönlendirmesi (port forwarding) ayarlamak için kullanılabilecek yöntemleri içerir.

## 1. `iptables` ile Port Yönlendirme

### 1.1. Port Yönlendirmesi Ayarlama

Aşağıdaki komut, belirli bir portu başka bir IP adresine yönlendirmek için kullanılabilir. Bu örnekte, 80 numaralı portu 192.168.1.100 IP adresine yönlendireceğiz:

```bash
sudo iptables -t nat -A PREROUTING -p tcp --dport 80 -j DNAT --to-destination 192.168.1.100:80
sudo iptables -A FORWARD -p tcp -d 192.168.1.100 --dport 80 -j ACCEPT
```

### 1.2. Yönlendirmeyi Kalıcı Hale Getirme

`iptables` ayarlarını kalıcı hale getirmek için şu komutu kullanabilirsiniz:

```bash
sudo iptables-save | sudo tee /etc/iptables/rules.v4
```
> **Not**: `iptables-persistent` paketini yüklemeniz gerekebilir:

```bash
sudo apt install iptables-persistent
```

## 2. `ufw` ile Port Yönlendirme

`ufw` (Uncomplicated Firewall) kullanarak port yönlendirmesi ayarlamak için aşağıdaki adımları izleyebilirsiniz.

### 2.1. `ufw`'yi Etkinleştirme

`ufw`'yi etkinleştirmek için:

```bash
sudo ufw enable
```

### 2.2. Port Yönlendirmesi Ayarlama

Port yönlendirmesi ayarlamak için aşağıdaki gibi bir kural ekleyebilirsiniz. Örneğin, 80 numaralı portu 192.168.1.100 IP adresine yönlendirmek için:

```bash
sudo ufw route allow proto tcp from any to 192.168.1.100 port 80
```

### 2.3. Yönlendirmeyi Kontrol Etme

Yönlendirme kurallarını kontrol etmek için:

```bash
sudo ufw status
```

## 3. NAT (Network Address Translation) Ayarları

Eğer yönlendirmeyi uygulayabilmek için NAT ayarlarına ihtiyacınız varsa, `sysctl` ile ayar yapabilirsiniz:

```bash
sudo sysctl -w net.ipv4.ip_forward=1
```

Bu ayarı kalıcı hale getirmek için `/etc/sysctl.conf` dosyasını açıp aşağıdaki satırı ekleyin:

```bash
net.ipv4.ip_forward = 1
```

## 4. Yönlendirmeyi Test Etme

Yönlendirmeyi test etmek için başka bir cihazdan yönlendirdiğiniz port üzerinden bağlantı yapmayı deneyin.
