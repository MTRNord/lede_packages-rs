include $(TOPDIR)/rules.mk

PKG_NAME:=iota
PKG_VERSION:=0.0.1
PKG_RELEASE:=1
PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE

PKG_REV:=f35d016c5b96328ef27cd4254393728b6786c5a7

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.xz
PKG_SOURCE_URL:=git://github.com/gchp/iota.git
PKG_SOURCE_PROTO:=git
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)
PKG_SOURCE_VERSION:=$(PKG_REV)

PKG_INSTALL:=1
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk

define Package/iota
  SUBMENU:=Editors
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=A terminal-based text editor written in Rust
  URL:=https://github.com/gchp/iota/
  MAINTAINER:=Greg Chapple <https://github.com/gchp>
endef

endef

define Build/Prepare
	$(call Build/Prepare/Default)
endef

define Package/iota/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(CP) $(PKG_INSTALL_DIR)/usr/bin/$(PKG_NAME) $(1)/usr/bin/
endef

$(eval $(call BuildPackage,iota))
