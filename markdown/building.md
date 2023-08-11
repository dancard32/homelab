# Building the Homelab

[Click Here](../README.md) to go back to the **README.md**

---

The first step to setting up the homelab - is building your homelab! I would recommend firstly getting a main computer server up and running and running your needed services and making sure the Virtual Machines's (VMs) are working so that you can test your development environment.

After this point I would expand to suit your needs and add switches, Network Interface Cards (NICs), Wireless Access Points (WAPs), Network Attached Storage (NAS) when best suited.

For a detailed description of my set-up (if you wish to repeat it verbatim) can be found below!

## Table of Contents

- [Bill of Materials](#bill-of-materials)
- [3D Printed Parts](#3d-printed-parts)
- [Assembling the Homelab](#assembling-the-homelab)

## Bill of Materials

Here you can find a detailed list of all the parts that I have in my homelab. If you have different functions in mind for your homelab I recommend tailoring this build to suit your needs and project requirements.

- **Server Rack**

  - [Kenuco SOHO Mini 10in 10in Half-width 9U Server Rack](https://www.amazon.com/KENUCO-Panels-Shelves-Components-White-9U/dp/B07QDPPPX7/ref=sr_1_3?crid=3J1702PNDA74T&keywords=kenuco%2B10u&qid=1691775398&sprefix=kenuco%2B10u%2B%2Caps%2C158&sr=8-3&ufe=app_do%3Aamzn1.fos.18ed3cb5-28d5-4975-8bc7-93deae8f9840&th=1)
  - [6in Telescopic Drawer Slides](<https://www.amazon.com/gp/your-account/order-history/ref=ppx_yo_dt_b_pagination_4_3?ie=UTF8&orderFilter=year-2023&search=&startIndex=20#:~:text=URBEST%20Ball%20Bearing%20Drawer%20Slides%20Full%20Extension%206%20Inch%20Telescopic%20Slider%20for%20Cabinet%2C%201Pair%20(6%2DInch)>)
  - [M6 Serrated Nuts](https://www.amazon.com/gp/product/B09MH9SP3T/ref=ppx_yo_dt_b_asin_title_o06_s00?ie=UTF8&psc=1)
  - [M6 x 10mm Button Head Socket Cap Bolts](https://www.amazon.com/gp/product/B09HC1MDM4/ref=ppx_yo_dt_b_asin_title_o06_s00?ie=UTF8&th=1)
  - [M5 x 6mm Button Head Hex Socket Cap Bolts](https://www.amazon.com/gp/product/B01AXUT5Q6/ref=ppx_yo_dt_b_asin_title_o06_s00?ie=UTF8&th=1)

- **Main Server Build**

  - **Main Computer**

    - [MSI Z270I GAMING PRO CARBON AC LGA 1151 Intel Z270 Mini ITX Intel Motherboard](https://www.newegg.com/p/N82E16813130972)
    - [Intel i7-6700k 4.0GHz LGA 1151 CPU](https://www.amazon.com/Intel-Processor-BX80662I76700K-Certified-Refurbished/dp/B07JQ3638R/ref=sr_1_2?crid=1OTL6AP4Q8IS3&keywords=intel+i7+6700k&qid=1691777533&sprefix=intel+i7+67%2Caps%2C162&sr=8-2)
    - [Noctua NH-L9i, Premium Low-Profile CPU Cooler](https://www.amazon.com/Noctua-NH-L9i-Premium-Low-profile-LGA115x/dp/B009VCAJ7W/ref=sr_1_3?crid=2JYZQT0WKGB4Z&keywords=lga+1151+slim+noctua+cooler&qid=1691777586&sprefix=lga+1151+slimnoctua+cooler%2Caps%2C142&sr=8-3)
    - [Corsair VENGEANCE LPX DDR4 RAM 32GB (2x16GB) 3200MHz RAM](https://www.amazon.com/gp/product/B07RW6Z692/ref=ppx_yo_dt_b_asin_title_o09_s00?ie=UTF8&th=1)
    - [4pcs Western Digital Blue 2TB - USED](https://www.amazon.com/gp/product/B08VH8R94B/ref=ppx_yo_dt_b_asin_title_o02_s00?ie=UTF8&th=1)
    - [970 Samsung EVO Plus](https://www.amazon.com/gp/product/B07MFZY2F2/ref=ppx_yo_dt_b_asin_title_o02_s00?ie=UTF8&th=1)
    - [Corsair SF Series, SF600, 600 Watt, SFX Modular PSU](https://www.amazon.com/Corsair-Platinum-Certified-Modular-Supply/dp/B07F84FJ1G/ref=sr_1_3?crid=NXJJGKYZ6117&keywords=corsair%2B600w%2Bmodular&qid=1691777644&sprefix=corsai%2B600w%2Bmodular%2Caps%2C109&sr=8-3&th=1)

  - [Power Switch](https://www.amazon.com/gp/product/B0986XLJJH/ref=ppx_yo_dt_b_asin_title_o00_s00?ie=UTF8&th=1)
  - [Reset Swtich](https://www.amazon.com/gp/product/B0BWDXFSMQ/ref=ppx_yo_dt_b_asin_title_o09_s00?ie=UTF8&psc=1)
  - [HDD Status LED](https://www.amazon.com/gp/product/B089RHBYGC/ref=ppx_yo_dt_b_asin_title_o00_s00?ie=UTF8&th=1)
  - [16 AWG Right Angle Power Cord](https://www.amazon.com/gp/product/B06Y6KHF4L/ref=ppx_yo_dt_b_asin_title_o08_s00?ie=UTF8&psc=1)
  - [SATA and Power Riser Adapter](https://www.amazon.com/gp/product/B08PQP6MZK/ref=ppx_yo_dt_b_asin_title_o07_s00?ie=UTF8&psc=1)

- **Networking**

  - [10Gbe NIC](https://www.amazon.com/gp/your-account/order-history/ref=ppx_yo_dt_b_pagination_3_2?ie=UTF8&orderFilter=year-2023&search=&startIndex=10#:~:text=10Gb%20PCI%2DE%20Network%20Card%20NIC%20Compatible%20for%20Intel%20X540%2DT2%2C%20Dual%20RJ45%20Copper%20Port%2C%20with%20Intel%20X540%2DBT2%20Controller%2C%20PCI%2DE%20X8%2C%2010G%20PCI%20Express%20LAN%20Adapter%20Support%20Windows%20Server/Windows/Linux/Vmware/ESX)
    - [Flexible PCI-E x8 Express Male to Female Slot Riser](https://www.amazon.com/gp/product/B08PCQPJHT/ref=ppx_yo_dt_b_asin_title_o02_s00?ie=UTF8&psc=1)
  - [SFP to RJ45 Transceiver](https://www.amazon.com/gp/product/B06XQBFHNL/ref=ppx_yo_dt_b_asin_title_o02_s00?ie=UTF8&psc=1)
  - [NICGIGA 2.5Gbe 5-port switch](https://www.amazon.com/dp/B0C53CB5CM?ref=nb_sb_ss_w_as-reorder-t1_k3_1_5&amp=&crid=VPMA54EJP8QI&amp=&sprefix=nicgi)
  - [Netgear 1Gbe 62W POE switch](https://www.amazon.com/gp/product/B08MBFLMDC/ref=ppx_yo_dt_b_asin_title_o08_s00?ie=UTF8&psc=1)
  - [Plastic RJ45 Ethernet Couplers](https://www.amazon.com/gp/product/B01JJ46JX4/ref=ppx_yo_dt_b_asin_title_o02_s00?ie=UTF8&th=1)
  - [_**Cosmetic Upgrade:**_ Zinc-Alloy RJ45 Ethernet Couplers](https://www.amazon.com/gp/product/B09VZZ6DWG/ref=ppx_yo_dt_b_asin_title_o01_s00?ie=UTF8&th=1)
  - [Amazon eero Pro 6E mesh Wi-Fi](https://www.amazon.com/gp/product/B091G68F8C/ref=ppx_yo_dt_b_asin_title_o03_s00?ie=UTF8&psc=1)

- **Raspberry Pi 4 Model B Cluster**

  - [Raspberry Pi 4 Model B - 4GB RAM](https://thepihut.com/products/raspberry-pi-4-model-b)
    - [If sold out check: https://rpilocator.com/](https://rpilocator.com/)
  - [3pcs x Isolated PoE HAT](https://www.amazon.com/gp/product/B08CVDQWXF/ref=ppx_yo_dt_b_asin_title_o01_s00?ie=UTF8&psc=1)
  - [_**Optional if not running headless**_ Mini HDMI to HDMI Connector](https://www.amazon.com/gp/product/B06WWQ7KLV/ref=ppx_yo_dt_b_asin_title_o00_s00?ie=UTF8&th=1)

- **Home Automation/IoT**

  - [Amazon Echo Dot (3rd Gen)](https://www.amazon.com/Echo-Dot/dp/B07PDHSLM6/ref=sr_1_14?crid=16D47ED5WZLWD&keywords=Amazon+echo+dot&qid=1691777269&sprefix=amazon+echo+dot%2Caps%2C116&sr=8-14)
  - [Google Nest Mini](https://www.bestbuy.com/site/nest-mini-2nd-generation-with-google-assistant-chalk/6348878.p?skuId=6348878&extStoreId=1092&ref=212&loc=1&gclid=Cj0KCQjwuNemBhCBARIsADp74QTHebpqr1n1e0H8t4fdqznFB7IvhMA7w_2LHum26O--PZAxyCUzrGAaAjG8EALw_wcB&gclsrc=aw.ds)

- **Miscellaneous**
  - [CyberPower 1500VA UPS System](https://www.amazon.com/gp/product/B00429N19W/ref=ppx_yo_dt_b_asin_title_o02_s01?ie=UTF8&th=1)
  - [White LED with MOLEX Connector](https://www.amazon.com/gp/product/B0B4G1THL9/ref=ppx_yo_dt_b_asin_title_o03_s00?ie=UTF8&psc=1)
  - [4pcs x 400mm T Slot 2020 Aluminum Extrusion](https://www.amazon.com/gp/product/B08Y8N7FD1/ref=ppx_yo_dt_b_asin_title_o02_s01?ie=UTF8&th=1)
  - [4pcs x 100mm T Slot 2020 Aluminum Extrusion](https://www.amazon.com/gp/product/B08TBLBXLV/ref=ppx_yo_dt_b_asin_title_o02_s00?ie=UTF8&th=1)

## 3D Printed Parts

**ADD LATER** BOM of 3D Printed Parts

## Assembling the Homelab

**ADD later documentation and have CAD drawings of assembly**

---

[Click Here](../README.md) to go back to the **README.md**
