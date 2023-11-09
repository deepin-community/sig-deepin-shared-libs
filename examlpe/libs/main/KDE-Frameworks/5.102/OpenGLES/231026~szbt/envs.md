export PATH="${kf5-DIR}/bin:/usr/local/bin:/usr/bin"

export LD_LIBRARY_PATH=${qt5-DIR}/lib:${kf5-DIR}/lib:${kf5-DIR}/lib/x86_64-linux-gnu:${dtk5-DIR}/lib

export QT_PLUGIN_PATH=${qt5-DIR}/plugins:${App-DIR}/lib/x86_64-linux-gnu/plugins:${kf5-DIR}/lib/x86_64-linux-gnu/plugins:${dtk5-DIR}/lib/qt5/plugins

export QT_QPA_PLATFORM_PLUGIN_PATH=${qt5-DIR}/plugins/platforms

export QML2_IMPORT_PATH=${qt5-DIR}/qml:${kf5-DIR}/lib/x86_64-linux-gnu/qml

export XDG_DATA_DIRS=${kf5-DIR}/share
