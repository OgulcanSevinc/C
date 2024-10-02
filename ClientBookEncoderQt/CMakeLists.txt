# CMakeLists.txt pour ClientBookEncoderQt

# Activer la politique CMP0079
cmake_policy(SET CMP0079 NEW)

# Trouver Qt
find_package(Qt5 COMPONENTS Widgets REQUIRED)

# Ajouter les fichiers sources et d'en-têtes
set(SOURCES
    main.cpp
    mainwindowclientbookencoder.cpp
    moc_mainwindowclientbookencoder.cpp
)

set(HEADERS
    mainwindowclientbookencoder.h
    ui_mainwindowclientbookencoder.h
)

# Ajouter un exécutable
add_executable(ClientBookEncoderQtApp ${SOURCES} ${HEADERS})

# Lier Qt à l'exécutable
target_link_libraries(ClientBookEncoderQtApp Qt5::Widgets)
