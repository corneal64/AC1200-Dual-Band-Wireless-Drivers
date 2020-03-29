# AC1200 Dual-Band USB 3.0 Wireless Adapter Drivers

### AC1200 Dual-Band Wireless Adapter Drivers [rtl88x2bu] [0bda:b812]

---

<img src="AC1200-Dual-Band-Wireless-Adapter.jpeg?raw=true" alt="Alt text" title="AC1200 Dual-Band Wireless Adapter" width="45%" />

## How to install

```bash
git clone https://github.com/corneal64/AC1200-Dual-Band-Wireless-Drivers.git

cd AC1200-Dual-Band-Wireless-Drivers

VER=$(sed -n 's/\PACKAGE_VERSION="\(.*\)"/\1/p' dkms.conf)

sudo rsync -rvhP ./ /usr/src/rtl88x2bu-${VER}

sudo dkms add -m rtl88x2bu -v ${VER}

sudo dkms build -m rtl88x2bu -v ${VER}

sudo dkms install -m rtl88x2bu -v ${VER}

sudo modprobe 88x2bu
```

