cmake_minimum_required(VERSION 3.18)        # требуемая версия cmake
project(    
    lesson5                                 # название проекта                        
    VERSION 0.0.0                           # номер версии проекта
    DESCRIPTION "Sixth project"             # описание           
    LANGUAGES CXX                           # язык программирования
)   
set(CMAKE_CXX_STANDARD 17)                  # устанавливаем требуемый стандарт языка (это значит, что в проекте буду использоваться фичи этоо стандарта)
set(CMAKE_CXX_STANDARD_REQUIRED ON)         # при сборке платформа будет проверять поддержку стандарта C++17 компилятором

set(CMAKE_BUILD_TYPE Debug)                 # конфигурация сборки - Debug

add_executable(lesson6)                     # эта команда сообщает платформе сборке, что код будет компилироваться в исполняемый файл с названием lesson5.exe

set(sources                                 # создаем cmake-переменную sources, которая содержит список файлов исходного когда (в данном случае main.cpp)
    main.cpp
)

target_sources(lesson6 PRIVATE ${sources})  # команда указывает компилятору, что исполняемый файл будет компилироваться из исходников, перечисленных в sources