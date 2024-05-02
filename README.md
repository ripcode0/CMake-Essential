# Modern CMake

- [CMake Stage](#CMAKE-STAGE)
- [Interface Library](#Interface-Library)
- [CMake 배치](#cmake-배치)
- [소스코드 조직화](#소스코드-조직화)


## CMake Stage

* CMake 의 프로세싱 절차
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
    - Test (Optional)              : 테스트 단계 (선택 사항)

    - Install (Optional)           : 설치 단계 (선택 사항) 
         - 생성 단계가 끝나면 바이너리 디렉토리에 cmake_install.cmake 가 생성
         - --install 명령어 를 통해 CMakeLists.txt 에 있는 install(..) 를 호출
         - --prefix 명령어를 통해 install 경로를 설정


## Interface Library

* 실제 실체가 없는 라이브러리다