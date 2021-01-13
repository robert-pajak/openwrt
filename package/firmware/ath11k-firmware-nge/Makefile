#
# Copyright (C) 2015 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=ath11k-firmware-nge
PKG_SOURCE_DATE:=2021-01-01
PKG_SOURCE_VERSION:=1
PKG_RELEASE:=1
USE_SOURCE=./base-files/IPQ8074

include $(INCLUDE_DIR)/package.mk

define Package/ath11k-firmware-nge-default
  SECTION:=firmware
  CATEGORY:=Firmware
  DEPENDS:=
endef

define Package/ath11k-firmware-nge-ipq8074
$(Package/ath11k-firmware-default)
  TITLE:=ath11k (nge) firmware for IPQ8074 devices
  SECTION:=firmware
  CATEGORY:=Firmware
endef

define Build/Compile

endef

define Package/ath11k-firmware-nge-ipq8074/install
	$(INSTALL_DIR) $(1)/lib/firmware/IPQ8074
	$(INSTALL_DATA) \
		$(PKG_BUILD_DIR)/IPQ8074/* \
		$(1)/lib/firmware/IPQ8074
endef

$(eval $(call BuildPackage,ath11k-firmware-nge-ipq8074))
