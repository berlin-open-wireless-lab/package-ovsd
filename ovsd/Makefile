include $(TOPDIR)/rules.mk

PKG_NAME:=ovsd
PKG_VERSION:=2016-08-18
PKG_RELEASE:=$(PKG_VERSION)

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/berlin-open-wireless-lab/ovsd.git
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)
PKG_SOURCE_VERSION:=cdfbfb4c0e7e665e547f0039e2e7b52dbb27e6ad
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION)-$(PKG_SOURCE_VERSION).tar.gz
PKG_MAINTAINER:=Arne Kappen <akappen@inet.tu-berlin.de>

PKG_BUILD_PARALLEL:=1

PKG_LICENSE:=GPL-2.0

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/cmake.mk


define Package/ovsd
  SECTION:=net
  CATEGORY:=Network
  DEPENDS:=+openvswitch +libubox +libubus +netifd
  TITLE:=Open vSwtich configuration daemon for netifd
  MAINTAINER:=Arne Kappen <akappen@inet.tu-berlin.de>
endef

define Package/ovsd/description
  External device handler adding Open vSwitch support to netifd.
endef

define Package/ovsd/install
	$(INSTALL_DIR) $(1)/sbin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/ovsd $(1)/sbin/
	$(CP) ./files/* $(1)/
endef

$(eval $(call BuildPackage,ovsd))
