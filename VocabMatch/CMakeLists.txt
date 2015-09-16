include_directories(
../lib/zlib
../lib/ann_1.1/include/ANN
../lib/ann_1.1_char/include/ANN
../lib/imagelib
../VocabLib)

file(GLOB VOCABMATCH_SOURCES "*.cpp")

add_executable(VocabMatch VocabMatch.cpp)
target_link_libraries(VocabMatch VocabLib imagelib ann_1.1 ann_1.1_char zlib)

add_executable(VocabMatch_desc VocabMatch_desc.cpp)
target_link_libraries(VocabMatch_desc VocabLib imagelib ann_1.1 ann_1.1_char zlib)

add_executable(VocabMatchScript VocabMatchScript.cpp)
target_link_libraries(VocabMatchScript VocabLib imagelib ann_1.1 ann_1.1_char zlib)

add_executable(VocabMatchScript_desc VocabMatchScript_desc.cpp)
target_link_libraries(VocabMatchScript_desc VocabLib imagelib ann_1.1 ann_1.1_char zlib)

