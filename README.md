* Memaksa Mode Performa Tinggi (High Performance):
  settings put global high_performance_mode 1
* Mematikan Thermal Service secara total:
  settings put global thermal_limit_constant 0
* Memaksa sirkuit thermal ke mode "Dingin" (Override Status):
  cmd thermal override-status 0
* Mengubah profil daya ke performa maksimal:
  settings put global power_idil_mode 0
* Mematikan fitur Adaptive Battery:
  settings put global adaptive_battery_management 0
(Daya bikin boros dan aplikasi ngak kepake bakal tidak dinonaktifkan sistem)
* Memaksa sistem pake Hardware Acceleration penuh untuk 2D/UI:
  settings put global hardware_accelerated_v2 true
* Memaksa GPU merender grafis secara penuh (Bypass CPU render):
  settings put global force_hw_ui true
* Mengurangi latensi pembacaan data memori internal (Trim otomatis):
  settings put global fstrim_mandatory 1
* Bypass Wi-Fi Throttling:
  settings put global wifi_scan_always_enabled 1
* Memaksa modul jaringan ke mode latency rendah:
  settings put global wifi_low_latency_mode_allowed 1
* Memaksa mesin compiler runtime pake mode performa maksimal:
  cmd package compile -m speed-profile -a
## 2. Whitelist Shizuku (Khusus Oppo/ColorOS)
* Masukin ke Whitelist Doze Mode:
  dumpsys deviceidle whitelist +moe.shizuku.privileged.api
* Bypass Battery Optimization:
  cmd power set-ignore-battery-optimization moe.shizuku.privileged.api