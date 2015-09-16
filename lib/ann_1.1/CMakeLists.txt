include_directories(./include)


IF (WIN32)
    ADD_DEFINITIONS ( -DDLL_EXPORTS -DANN_PERF -DANN_NO_RANDOM
-D_CRT_SECURE_NO_DEPRECATE )
    SET ( LIBRARY_TYPE SHARED )
ELSE (WIN32)
    SET ( LIBRARY_TYPE STATIC )
ENDIF (WIN32)

# list sources files
FILE(GLOB LIBRARY_FILES_CPP "src/*.cpp")
FILE(GLOB LIBRARY_FILES_H "include/*.h")

ADD_LIBRARY(ann_1.1
${LIBRARY_FILES_CPP}
${LIBRARY_FILES_H}
)

remove_definitions()

ADD_EXECUTABLE ( ann_test
  ./test/ann_test.cpp
  ./test/rand.cpp
)

ADD_EXECUTABLE ( ann_sample
  ./sample/ann_sample.cpp
)

ADD_EXECUTABLE ( ann2fig
  ./ann2fig/ann2fig.cpp
)

TARGET_LINK_LIBRARIES ( ann_test ann_1.1 )

TARGET_LINK_LIBRARIES ( ann_sample ann_1.1 )

TARGET_LINK_LIBRARIES ( ann2fig ann_1.1 )

