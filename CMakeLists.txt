project(kwebkitpart)

# search packages used by KDE
find_package(ECM REQUIRED)
set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} ${ECM_MODULE_PATH})
include(KDEInstallDirs)
include(KDECMakeSettings)
include(KDECompilerSettings)
include(FeatureSummary)

find_package(Qt5 ${QT_MIN_VERSION} CONFIG REQUIRED COMPONENTS Core DBus Gui Widgets WebKit WebKitWidgets UiTools)
find_package(KF5 ${KF5_MIN_VERSION} REQUIRED Archive Bookmarks CoreAddons Config ConfigWidgets DBusAddons KIO KDELibs4Support Parts Activities WebKit I18n)
find_package(KF5Parts)
find_package(KF5Sonnet)
include(MacroLibrary)
add_definitions(-DQT_USE_FAST_CONCATENATION -DQT_USE_FAST_OPERATOR_PLUS)


add_subdirectory(icons)
add_subdirectory(src)
add_subdirectory(kdelauncher)
