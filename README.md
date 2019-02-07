# PIO-ESP-ADF

ESP-ADF for PlatformIO projects.

# Usage

1. Copy the `lib` directory and its contents to the root of your PIO project
2. Add the following to `platformio.ini`:
```
build_flags =
  -D CONFIG_ESP_LYRAT_V4_3_BOARD
  -I lib/audio_hal/include
  -I lib/audio_hal/board
  -I lib/audio_hal/driver/es8374
  -I lib/audio_hal/driver/es8388
  -I lib/audio_hal/driver/zl38063
  -I lib/audio_hal/driver/zl38063/api_lib
  -I lib/audio_hal/driver/zl38063/example_apps
  -I lib/audio_hal/driver/zl38063/firmware
  -L lib/audio_hal/driver/zl38063/firmware
  -lfirmware
  -I lib/audio_pipeline/include
  -I lib/audio_sal/include
  -I lib/audio_service/include
  -I lib/audio_stream/include
  -I lib/esp-adf-libs/esp_audio/include
  -L lib/esp-adf-libs/esp_audio/lib
  -I lib/esp-adf-libs/esp_codec/include/codec
  -I lib/esp-adf-libs/esp_codec/include/processing
  -L lib/esp-adf-libs/esp_codec/lib
  -lesp_codec
  -I lib/esp-adf-libs/esp_dlna/include
  -L lib/esp-adf-libs/esp_dlna/lib
  -I lib/esp-adf-libs/esp_sr/include
  -L lib/esp-adf-libs/esp_sr/lib
  -I lib/esp-adf-libs/esp_ssdp/include
  -L lib/esp-adf-libs/esp_ssdp/lib
  -I lib/esp-adf-libs/esp_upnp/include
  -L lib/esp-adf-libs/esp_upnp/lib
  -I lib/esp-adf-libs/recorder_engine/include
  -L lib/esp-adf-libs/recorder_engine/lib
  -I lib/esp_peripherals/driver/i2c_bus
  -I lib/esp_peripherals/include
  -I lib/esp_peripherals/lib/adc_button
  -I lib/esp_peripherals/lib/blufi
  -I lib/esp_peripherals/lib/button
  -I lib/esp_peripherals/lib/IS31FL3216
  -I lib/esp_peripherals/lib/sdcard
  -I lib/esp_peripherals/lib/touch
  -I lib/esp_http_client/include
  -I lib/esp_http_client/lib/include
  -I lib/tcp_transport/include
lib_archive = false
build_unflags = -I "<path to .platformio>/packages/framework-espidf/components/esp_http_client/include"
lib_deps =
  audio_hal
  audio_pipeline
  audio_sal
  audio_service
  audio_stream
  esp_audio
  esp_codec
  esp_dlna
  esp_sr
  esp_ssdp
  esp_upnp
  recorder_engine
  esp_peripherals
  esp_http_client
```
3. Replace `<path to .platformio>` in `build_unflags` with the path to your PlatformIO home directory.
