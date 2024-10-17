# ESP32_arduino_a2dp_ble_coex
thanks for https://github.com/pschatzmann/ESP32-A2DP and merge expressif official lib a2dp_gatts_coex

1 move .cpp .h to ESP32-A2DP_main/src

2 modify BluetoothA2DPCommon.cpp 
  change mode to ESP_BT_MODE_BTDM of BluetoothA2DPCommon::bt_start

3 modify project.ino 
  #include "coex_BLE.h"
  
4 alfter a2dp_sink.start("MyMusic");
  ADD ble_gatts_init();

5 done.
  
