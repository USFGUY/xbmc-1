set(SOURCES Peripheral.cpp
            PeripheralBluetooth.cpp
            PeripheralDisk.cpp
            PeripheralHID.cpp
            PeripheralImon.cpp
            PeripheralJoystick.cpp
            PeripheralKeyboard.cpp
            PeripheralNIC.cpp
            PeripheralNyxboard.cpp
            PeripheralTuner.cpp)

set(HEADERS Peripheral.h
            PeripheralBluetooth.h
            PeripheralDisk.h
            PeripheralHID.h
            PeripheralImon.h
            PeripheralJoystick.h
            PeripheralKeyboard.h
            PeripheralNIC.h
            PeripheralNyxboard.h
            PeripheralTuner.h)

if(CEC_FOUND)
  list(APPEND SOURCES PeripheralCecAdapter.cpp)
  list(APPEND HEADERS PeripheralCecAdapter.h)
endif()

core_add_library(peripherals_devices)
