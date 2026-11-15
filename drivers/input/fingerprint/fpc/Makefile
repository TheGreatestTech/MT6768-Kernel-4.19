#
# Makefile for the fingerprint device.
#

# Each configuration option enables a list of files.
#include $(srctree)/drivers/misc/mediatek/Makefile.custom
ccflags-y += -I$(srctree)/drivers/input/fingerprint/goodix
ccflags-y += -I$(srctree)/drivers/spi/mediatek/$(MTK_PLATFORM)
ccflags-y += -I$(srctree)/drivers/misc/mediatek/include
ccflags-y += -I$(srctree)/drivers/misc/mediatek/include/mt-plat
ccflags-y += -I$(srctree)/drivers/misc/mediatek/include/mt-plat/$(MTK_PLATFORM)/include
ccflags-y += -I$(srctree)/drivers/misc/mediatek/base/power/include/
ccflags-y += -I$(srctree)/drivers/misc/mediatek/base/power/$(MTK_PLATFORM)/
ccflags-y += -I$(srctree)/drivers/devfreq/
subdir-ccflags-y += -I$(srctree)/drivers/tee/teei/400/tz_driver/include
subdir-ccflags-y += -I$(srctree)/drivers/tee/teei/400/common/include/
ifdef CONFIG_TARGET_PRODUCT_FIRE
obj-$(CONFIG_FPC_FINGERPRINT) += mtk_spi.o
else
obj-$(CONFIG_FPC_FINGERPRINT)	+= fpc1022_tee.o
endif

# TODO: Combine both drivers, it look same but mtk_spi is better