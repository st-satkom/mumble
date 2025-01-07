# Minimum CMake sürümünü belirtiyoruz
cmake_minimum_required(VERSION 3.12)

# Proje adı ve dili
project(MyProject VERSION 1.0 LANGUAGES CXX)

# C++ standardını belirtiyoruz
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Kaynak dosyalarını belirtiyoruz
set(SOURCES
    src/main.cpp
    src/helper.cpp
)

# Başlık dosyalarını belirtiyoruz
set(HEADERS
    include/helper.h
)

# Çıktı dosyasını oluşturuyoruz
add_executable(${PROJECT_NAME} ${SOURCES})

# Include dizinlerini bağlıyoruz
target_include_directories(${PROJECT_NAME} PRIVATE include)

# Gerekirse kütüphaneler ekleyin
# Örnek: target_link_libraries(${PROJECT_NAME} PRIVATE SomeLibrary)
