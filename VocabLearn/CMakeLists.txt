include_directories(
../lib/zlib
../lib/ann_1.1/include/ANN
../lib/ann_1.1_char/include/ANN
../lib/imagelib
../VocabLib)

add_executable(VocabLearn VocabLearn.cpp)

target_link_libraries(VocabLearn VocabLib imagelib ann_1.1 ann_1.1_char zlib)