include_directories(
../lib/zlib
../lib/ann_1.1/include/ANN
../lib/ann_1.1_char/include/ANN
../lib/imagelib)

FILE(GLOB VOCABLIB_HEADERS "*.h")
FILE(GLOB VOCABLIB_SOURCES "*.cpp")

add_library(VocabLib ${VOCABLIB_HEADERS} ${VOCABLIB_SOURCES})