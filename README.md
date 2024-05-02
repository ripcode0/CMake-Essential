# Modern CMake

- [CMAKE STAGE](#CMAKE-단계)
- [INTERFACE LIBRARY](#INTERFACE-LIBRARY)
- [CMake 배치](#cmake-배치)
- [소스코드 조직화](#소스코드-조직화)


## CMAKE 단계

* Proccesing CMakeLists.txt    : 프로세싱 단계
    - Configure         : 구성 단계
    ```cmd
    cmake -S . -B build
    #-S Root CMakeLists.txt 있는 위치
    #-B 바이너리 파일들이 생성될 위치
    ```
    - Generate          : 생성 단계
    ```cmd
    Processing CMakeLists.txt
    -- Configuring done
    -- Generating done
    ```
    - Build             : 빌드 단계
    ```cmd
    cmake --build build --config <Debug or Release>
    ```