include $(TOPDIR)/rules.mk

PKG_NAME:=autoupdater
PKG_VERSION:=2

PKG_BUILD_DIR := $(BUILD_DIR)/$(PKG_NAME)

include $(INCLUDE_DIR)/package.mk

define Package/autoupdater
  SECTION:=admin
  CATEGORY:=Administration
  DEPENDS:=+lua-platform-info +libuci-lua +luci-lib-nixio +ecdsautils +!BUSYBOX_CONFIG_SHA256SUM:coreutils-sha256sum
  TITLE:=Automatically update firmware
endef

define Build/Prepare
	mkdir -p $(PKG_BUILD_DIR)
endef

define Build/Configure
endef

define Build/Compile
endef

define Package/autoupdater/install
	$(CP) ./files/* $(1)/
endef

$(eval $(call BuildPackage,autoupdater))
