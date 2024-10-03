## İşletim sistemi bilgilerinin alınması
sudo cat /etc/os-release

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
sudo cat /proc/cpuinfo

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
