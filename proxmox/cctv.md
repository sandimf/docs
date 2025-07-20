---
description: Ini adalah dokumentasi bagaimana memasang cctv pada server proxmox.
---

# CCTV

{% embed url="https://nxvms.com/" %}

## Setting Up a CCTV Server with NX Witness via Proxmox

### Langkah 1: Memulai Proses

Untuk mengatur server CCTV, Anda memerlukan perangkat lunak NX Witness bersama dengan skrip pembantu Proxmox.

### Langkah 2: Instal NX Witness

\
Selanjutnya, akses server Proxmox Anda. Setelah masuk, pilih opsi "Shell" pada antarmuka server.

<figure><img src="../.gitbook/assets/Screen Shot 2025-07-20 at 20.57.54.png" alt=""><figcaption></figcaption></figure>

Seteleh membuka shell Anda bisa menggunakan script ini untuk menginstall atau mendapatkannya dari proxmox helper.

```bash
bash -c "$(curl -fsSL https://raw.githubusercontent.com/community-scripts/ProxmoxVE/main/ct/nxwitness.sh)"
```

### Langkah 3: Konfigurasi NX Witness



