#
# Copyright (C) 2007-2010 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#
include $(TOPDIR)/rules.mk

PKG_NAME:=hello
PKG_VERSION:=2.10
PKG_RELEASE:=1

PKG_BUILD_DIR:=$(BUILD_DIR)/$(PKG_NAME)T)/$(PKG_NAME)-$(PKG_VERSION)
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=@GNU/$(PKG_NAME)
#PKG_MD5SUM:=1bb3a1d98b1973aee6e8f171933c0f61

PKG_MAINTAINER:=Reuben Thomas and Sami Kerola <bug-hello@gnu.org>
PKG_LICENSE:=GPL

PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk

define Package/hello
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=The GNU Hello program produces a familiar, friendly greeting.
  URL:=https://www.gnu.org/software/hello/
endef

define Package/hello/description
GNU Hello is written in C. 
For implementations in other programming languages, 
notably including translation into other languages, 
please see the GNU Gettext distribution.
endef

define Package/hello/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/$(PKG_NAME) $(1)/usr/bin/$(PKG_NAME)
endef

$(eval $(call BuildPackage,hello))
