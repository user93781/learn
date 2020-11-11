# `vcpkg`

## Repology

- Use Repology to find all the packages that `vcpkg` supports.
  - https://repology.org/projects/?inrepo=vcpkg
- Alternatively: https://github.com/microsoft/vcpkg/tree/master/ports
- To install, go the project page, and scroll until you find **vcpkg**.
  - https://repology.org/project/cairo/versions

## Usage

```cmake
cmake_minimum_required(VERSION 3.8)

project(<project_name>)

find_package(unofficial-sodium CONFIG REQUIRED)

add_executable(main main.cpp)

target_link_libraries(main PRIVATE unofficial-sodium::sodium)
```

```bash
mkdir build
cd build
cmake .. "-DCMAKE_TOOLCHAIN_FILE=~/vcpkg/scripts/buildsystems/vcpkg.cmake"
```

## Packages

### `sqlite3`

```cmake
find_package(unofficial-sqlite3 CONFIG REQUIRED)
target_link_libraries(main PRIVATE unofficial::sqlite3::sqlite3)
```
