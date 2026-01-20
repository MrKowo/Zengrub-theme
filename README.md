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

## 🛠 Customization (Size & Scaling)

If the icons or the menu look too small (common on 4K screens) or too large, you can adjust the elements in the `theme.txt` file.

### Adjusting Element Sizes

Open the theme file:

```bash
sudo nano /boot/grub2/themes/zengrub/theme.txt

```

#### 1. The Boot Menu Box

Look for the `+ boot_menu` section. To make the menu larger on high-res screens, increase the `width` and `height`:

```text
+ boot_menu {
  left = 30%
  top = 40%
  width = 40%   # Increase this (e.g., 50%) for a wider menu
  height = 30%  # Increase this for more vertical space
  ...
}

```

#### 2. The ASUS Spinner

To change the size or position of the loading animation, look for the `+ image` section containing `spinner.png`:

```text
+ image {
  top = 70%     # Change vertical position (0% is top, 100% is bottom)
  left = 48%    # Change horizontal position
  width = 64    # Increase this (e.g., 128) for a larger spinner
  height = 64   # Match the width to keep it circular
  file = "spinner.png"
}

```

#### 3. Font Size

If the text is unreadable, find the `item_font` or `font` lines. You can point them to a larger `.pf2` font file or use a tool like `grub-mkfont` to generate a larger version of your preferred font.

---

**Disclaimer:** *Always keep a live USB handy when editing GRUB configurations. This theme is a community project and is not affiliated with ASUS.*
