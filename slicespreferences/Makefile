ARCHS = armv7 armv7s arm64 arm64e
ADDITIONAL_OBJCFLAGS = -fobjc-arc

include $(THEOS)/makefiles/common.mk

BUNDLE_NAME = SlicesPreferences
SlicesPreferences_FILES = SliceDetailController.mm SlicesEditableTableCell.mm ../Model/SSKeychain/SSKeychain.m ../Model/GameCenterAccountManager.mm ../Model/AppGroupSlicer.mm ../Model/RawSlicer.mm ../Model/Slicer.mm ../Model/FolderMigrator.mm ../Model/SliceSetting.mm GameCenterController.mm SlicesPreferencesListController.mm SlicesAppController.mm SlicesAppDetailController.mm
SlicesPreferences_INSTALL_PATH = /Library/PreferenceBundles
SlicesPreferences_FRAMEWORKS = Social Security GameKit UIKit
SlicesPreferences_PRIVATE_FRAMEWORKS = Preferences BackBoardServices
SlicesPreferences_LIBRARIES = applist

include $(THEOS)/makefiles/bundle.mk

internal-stage::
	$(ECHO_NOTHING)mkdir -p $(THEOS_STAGING_DIR)/Library/PreferenceLoader/Preferences$(ECHO_END)
	$(ECHO_NOTHING)cp entry.plist $(THEOS_STAGING_DIR)/Library/PreferenceLoader/Preferences/SlicesPreferences.plist$(ECHO_END)
