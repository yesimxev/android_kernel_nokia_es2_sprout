ifeq ($(CONFIG_MTK_GAUGE_VERSION),30)
subdir-ccflags-y += -I$(srctree)/drivers/misc/mediatek/usb_c/tcpc/inc
subdir-ccflags-y += -I$(srctree)/drivers/power/mediatek/charger
else
subdir-ccflags-y += -I$(srctree)/drivers/misc/mediatek/power/mt6755
endif

ifneq (user,$(TARGET_BUILD_VARIANT))
subdir-ccflags-y += -DCONFIG_DEBUG_REG
endif

obj-$(CONFIG_MFD_RT5081A_PMU)		+= rt5081a_pmu_i2c.o rt5081a_pmu_regmap.o\
					rt5081a_pmu_irq.o rt5081a_pmu_subdevs.o\
					rt5081a_pmu_core.o
obj-$(CONFIG_RT5081A_PMU_LDO)		+= rt5081a_pmu_ldo.o
obj-$(CONFIG_RT5081A_PMU_DSV)		+= rt5081a_pmu_dsv.o
obj-$(CONFIG_RT5081A_PMU_FLED)		+= rt5081a_pmu_fled.o
obj-$(CONFIG_RT5081A_PMU_BLED)		+= rt5081a_pmu_bled.o
obj-$(CONFIG_RT5081A_PMU_RGBLED)		+= rt5081a_pmu_rgbled.o

ifeq ($(CONFIG_MTK_GAUGE_VERSION),30)
obj-$(CONFIG_RT5081A_PMU_CHARGER)	+= rt5081a_pmu_charger.o
else
obj-$(CONFIG_RT5081A_PMU_CHARGER)	+= rt5081a_pmu_charger_gm20.o
endif
