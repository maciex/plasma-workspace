add_definitions(-DTRANSLATION_DOMAIN=\"kio5_applications\")

add_library(kio_applications MODULE kio_applications.cpp)

target_link_libraries(kio_applications KF5::KIOCore KF5::I18n)

install(TARGETS kio_applications  DESTINATION ${KDE_INSTALL_PLUGINDIR} )
install( FILES  programs.protocol applications.protocol  DESTINATION  ${KDE_INSTALL_KSERVICES5DIR} )
