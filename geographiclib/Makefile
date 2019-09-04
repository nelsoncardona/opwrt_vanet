#
# Copyright (C) 2009-2010 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=GeographicLib
PKG_VERSION:=1.49

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://sourceforge.net/projects/geographiclib/files/distrib/
PKG_MD5SUM:=26ec965354126d42ee3b8e9cf62f8af5


#PKG_FIXUP:=autoreconf
#PKG_REMOVE_FILES:=aclocal.m4 GNUmakefile
#PKG_INSTALL:=1

include $(INCLUDE_DIR)/package.mk

define Package/GeographicLib
  SECTION:=libs
  CATEGORY:=Libraries
#  DEPENDS:=+libpthread +libstdcpp
  TITLE:=GeographicLib offers a C++ interfaces to a small (but important!) set of geographic transformations.
  URL:=https://geographiclib.sourceforge.io/html/index.html
endef

define Package/package/Geographiclib
  GeographicLib offers a C++ interfaces to a small (but important!) set of geographic transformations.
endef

#CONFIGURE_ARGS += \
#	--enable-static \
#	--enable-shared

#TARGET_LDFLAGS += \
#	-lpthread

define Build/InstallDev
	$(INSTALL_DIR) $(1)/usr/include/GeographicLib
	$(CP) $(PKG_INSTALL_DIR)/usr/include/GeographicLib--/* $(1)/usr/include/GeographicLib/
	$(INSTALL_DIR) $(1)/usr/lib
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/libGeographic.{a,so*} $(1)/usr/lib/
endef

define Package/Geographiclib/install
	$(INSTALL_DIR) $(1)/usr/lib
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/libGeographic.so* $(1)/usr/lib/
endef

$(eval $(call BuildPackage,Geographiclib))
