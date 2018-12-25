# PIO-ESP-ADF

ESP-ADF for PlatformIO projects.

# Usage

1. Copy the `lib` directory and its contents to the root of your PIO project
2. Add the following to `platformio.ini`:
```
build_flags =
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
  -I lib/esp_audio/include
  -L lib/esp_audio/lib
  -I lib/esp_codec/include/codec
  -I lib/esp_codec/include/processing
  -L lib/esp_codec/lib
  -lesp_codec
  -I lib/esp_peripherals/include
  -I lib/esp_peripherals/lib/button
  -I lib/esp_peripherals/lib/sdcard
  -I lib/esp_peripherals/lib/touch
  -I lib/esp_sr/include
  -L lib/esp_sr/lib
  -I lib/recorder_engine/include
  -L lib/recorder_engine/lib
lib_archive = false
lib_deps =
  audio_hal
  audio_pipeline
  audio_sal
  audio_service
  audio_stream
  esp_audio
  esp_codec
  esp_peripherals
  esp_sr
  recorder_engine
```
