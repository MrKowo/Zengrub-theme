<p align="center">
  <img src="assets/preview.png" alt="ZenGrub Preview" width=10%>
</p>

# ZenGrub
A high-quality bootloader theme for GRUB2, inspired by the ASUS Zenbook aesthetic and based on the "spinner" theme.

<p align="center">
  <img src="assets/boot.png" alt="ZenGrub Preview" width=100%>
</p>

## 🚀 Installation

### 1. Clone the repository

```bash
git clone https://github.com/MrKowo/Zengrub-theme.git
cd Zengrub-theme

```

### 2. Move to GRUB directory

Create the themes folder if it doesn't exist and copy the files:

```bash
sudo mkdir -p /boot/grub2/themes/zengrub
sudo cp -r * /boot/grub2/themes/zengrub/

```

*(Note: On some distributions, the path is `/boot/grub/themes/`)*

### 3. Edit GRUB configuration

Open your GRUB configuration file:

```bash
sudo nano /etc/default/grub

```

Add or modify the following lines:

```text
GRUB_THEME="/boot/grub2/themes/zengrub/theme.txt"
GRUB_GFXMODE="auto"

```

*(Tip: For best results on high-res screens, set `GRUB_GFXMODE` to your native resolution, e.g., `1920x1080` or `3840x2160`)*

### 4. Update GRUB

**Fedora:**

```bash
sudo grub2-mkconfig -o /boot/grub2/grub.cfg

```

**Ubuntu/Debian/Mint:**

```bash
sudo update-grub

```

---

**Disclaimer:** *Always keep a live USB handy when editing GRUB configurations. This theme is not affiliated with ASUS.*
