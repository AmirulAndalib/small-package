#=====================================================================================================
# This file is licensed under the terms of the GNU General Public
# License version 2. This program is licensed "as is" without any
# warranty of any kind, whether express or implied.
#
# This file is a part of the luci-app-amlogic plugin
# https://github.com/ophub/luci-app-amlogic
#
# Description: Supports install/update/backup/restore/snapshot operations using OpenWrt on many boxes
# Copyright (C) 2021- https://github.com/unifreq/openwrt_packit
# Copyright (C) 2021- https://github.com/ophub/luci-app-amlogic
#
# Command: curl -fsSL git.io/luci-app-amlogic | bash
#=====================================================================================================

include $(TOPDIR)/rules.mk

PKG_NAME:=luci-app-amlogic
PKG_VERSION:=3.1.263
PKG_RELEASE:=1

PKG_LICENSE:=GPL-2.0 License
PKG_MAINTAINER:=ophub <https://github.com/ophub/luci-app-amlogic>

LUCI_TITLE:=LuCI support for Amlogic, Allwinner and Rockchip related boxs
LUCI_PKGARCH:=all
LUCI_DEPENDS:= \
	@(aarch64||arm) +bash +blkid +block-mount +busybox +curl +dosfstools +e2fsprogs \
	+fdisk +jq +losetup +luci +luci-lib-nixio +lsblk +parted +perl +pv +uuidgen

define Package/$(PKG_NAME)/conffiles
/etc/config/amlogic
endef

include $(TOPDIR)/feeds/luci/luci.mk

# call BuildPackage - OpenWrt buildroot signature
