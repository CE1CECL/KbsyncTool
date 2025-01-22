TARGET := iphone:clang:10.3:3.0
ARCHS = armv7
GO_EASY_ON_ME = 1
# THEOS_DEVICE_IP = 127.0.0.1
# THEOS_DEVICE_PORT = 58422

include $(THEOS)/makefiles/common.mk

TOOL_NAME = kbsynctool

kbsynctool_FILES = main.m $(wildcard GCDWebServer/*/*.m)
kbsynctool_CFLAGS = -fobjc-arc -IGCDWebServer/Core -IGCDWebServer/Requests -IGCDWebServer/Responses
kbsynctool_LIBRARIES = rocketbootstrap z
kbsynctool_FRAMEWORKS = CFNetwork CoreServices UIKit
kbsynctool_PRIVATE_FRAMEWORKS = AppSupport
kbsynctool_CODESIGN_FLAGS = -Sentitlements.plist
kbsynctool_INSTALL_PATH = /usr/local/bin

include $(THEOS_MAKE_PATH)/tool.mk
