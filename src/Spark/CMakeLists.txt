set(INCROOT ${PROJECT_SOURCE_DIR}/include/${PROJECT_NAME})
set(SRCROOT ${PROJECT_SOURCE_DIR}/src/${PROJECT_NAME})

set(SRC
    ${INCROOT}/ThreadPool.hpp
    ${SRCROOT}/ThreadPool.cpp
)

add_library(${PROJECT_NAME} STATIC ${SRC}) 

set_target_properties(${PROJECT_NAME} PROPERTIES LINKER_LANGUAGE CXX CXX_STANDARD 17)
target_include_directories(${PROJECT_NAME} PUBLIC ${PROJECT_SOURCE_DIR}/include)
