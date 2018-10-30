# Add 1k of padding to the DTBs to allow for environment variables
# to be runtime added by the bootloader (i.e. /chosen properties)
DTC_FLAGS += -p 1024

dtbo-$(CONFIG_SURFNA_DTB) += msm8940-surfna-evt-overlay.dtbo

ifeq ($(CONFIG_BUILD_ARM64_DT_OVERLAY),y)
msm8940-surfna-evt-overlay.dtbo-base := \
	msm8940-surfna-base.dtb
endif

always		:= $(dtb-y)
subdir-y	:= $(dts-dirs)
clean-files	:= *.dtb
