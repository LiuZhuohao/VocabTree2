include_directories(
../lib/zlib
../lib/ann_1.1/include/ANN
../lib/ann_1.1_char/include/ANN
../lib/imagelib)

ADD_LIBRARY(imagelib
qsort.c util.c
)