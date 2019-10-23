PROGRAM = main

EXTRA_COMPONENTS = \
	extras/http-parser \
	extras/dhcpserver \
  $(abspath ../../components/esp-8266/wifi_config) \
	$(abspath ../../components/esp-8266/cJSON) \
	$(abspath ../../components/common/wolfssl) \
	$(abspath ../../components/common/homekit)

FLASH_SIZE ?= 32
REED_PIN ?= 4
RELAY_PIN ?= 2

EXTRA_CFLAGS += -I../.. -DHOMEKIT_SHORT_APPLE_UUIDS -DREED_PIN=$(REED_PIN) -DRELAY_PIN=$(RELAY_PIN)


include $(SDK_PATH)/common.mk

monitor:
	$(FILTEROUTPUT) --port $(ESPPORT) --baud 9600 --elf $(PROGRAM_OUT)
