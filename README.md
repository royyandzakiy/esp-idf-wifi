# ESP IDF WiFi - Basic

This is a basic implementation of the [WiFi Station example from esp idf SDK](https://github.com/espressif/esp-idf/blob/release/v4.4/examples/wifi/getting_started/station/) with some changes to make it work for ESP IDF `release/v4.4.1`.

## IMPORTANT: 
I use ESP IDF in **release/v4.4.1**, other versions may or may not work accordingly

## Getting Started
- prepare your ESP IDF, make sure it uses the version `release/v4.4.1` or any other releases that would comply
- clone this repo `git clone https://github.com/royyandzakiy/esp-idf-wifi`
- start the idf configuration
    - if you use the ESP IDF extension in VSCode, just click on the gear icon
    - if you use cli, do `idf.py menuconfig` (i will assume, you have gotten idf.py working with the `{IDF PATH}/export.sh`)
- under WiFi Configuration change these parameters:
    - WiFi SSID
    - WiFi Password (keep empty if there is none)
- Build, Flash, Monitor
- enjoy!

---

## Changes
I made some changes, because incompatibility of usage of the `wifi_sta_config_t` from the original example (i think it uses a different esp idf version, haven't tracked which version it implements though). Adding these changes will make it work
```
.sae_pwe_h2e = WPA3_SAE_PWE_BOTH,
```

I also changed the config title to `WiFi Configuration`