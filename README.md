# LOKALISASI-DAN-PEMETAAN
AXCEEL ARKINDO - 4222201057

# Studi Kasus
Robot bertugas mengantarkan barang dari Ruang 203 ke Lobby BRAIL di Lantai 2 Gedung Utama
Politeknik Negeri Batam. Robot harus mampu melakukan lokalisasi, pemetaan, dan navigasi
otonom menggunakan ROS. Untuk mensimulasikan proses pengantaran barang, gunakan
indikator buzzer dengan ketentuan berikut:

• Saat robot mencapai lokasi pick (Ruang 203) dan “mengambil barang”, dengan indikator
buzzer berbunyi 1 kali atau suara dari speaker.

• Saat robot mencapai lokasi place (Lobby BRAIL) dan “mengantarkan barang”, buzzer
berbunyi 2 kali atau suara dari speaker

# Turtlebo4 Navigation dari Point A ke Point B

Proyek ini dibuat untuk ujian tengah semester, tujuannya adalah bergerak ke titik A, menyalakan buzzer satu kali, kemudian pergi ke titik B dan menyalakan buzzer dua kali.

```bash
mkdir ~/kelompok_dava/src
cd ~/kelompok_dava/src
```


### Instal package dan dependencies
```bash
cd ../ && rosdep install --from-paths src --ignore-src -r -y
```

### Sambungkan pc dan turtlebot (Via Ethernet)
```bash
ssh ubuntu@192.168.185.3
```

### Melakukan Mapping
```bash
ros2 launch turtlebot4_navigation slam.launch.py
ros2 launch turtlebot4_viz view_robot.launch.py
```

# Menjalankan Nav2

### Menjalankan Lokalisasi
```bash
source install/setup.bash
ros2 launch kelompok_davalocalization.launch.py
```

 ### Menjalankan Navigasi
```bash
source install/setup.bash
ros2 launch kelompok-dava run_nav.launch.py
```


### Menjalankan RViz
```bash
ros2 launch turtlebot4_viz view_navigation.launch.py
```


### Menjalankan Program goal point to point
```bash
source install/setup.bash
ros2 run kelompok_dava kelompok_dava
```
