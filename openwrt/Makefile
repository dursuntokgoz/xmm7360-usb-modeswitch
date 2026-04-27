include $(TOPDIR)/rules.mk

PKG_NAME:=xmm7360-usb-modeswitch
PKG_VERSION:=1.0
PKG_RELEASE:=1

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/dursuntokgoz/xmm7360-usb-modeswitch.git
PKG_SOURCE_VERSION:=main

include $(INCLUDE_DIR)/package.mk

define Package/xmm7360-usb-modeswitch
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=XMM7360 USB modeswitch tool
endef

define Package/xmm7360-usb-modeswitch/description
 Tool for switching Intel XMM7360 modem modes
endef

define Build/Compile
    $(MAKE) -C $(PKG_BUILD_DIR) \
        CC="$(TARGET_CC)" \
        CFLAGS="$(TARGET_CFLAGS)"
endef

define Package/xmm7360-usb-modeswitch/install
    $(INSTALL_DIR) $(1)/usr/bin
    $(INSTALL_BIN) $(PKG_BUILD_DIR)/xmm7360-usb-modeswitch $(1)/usr/bin/
endef

$(eval $(call BuildPackage,xmm7360-usb-modeswitch))
