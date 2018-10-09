#moveniu http module CmakeLists.txt -- libmoveniu_http.a

set(LIB_MOVENIU_HTTP moveniu_http)
aux_source_directory(${MOVENIU_SRC_DIR}/3rd/http/ HTTP_SRC)

add_library(${LIB_MOVENIU_HTTP} ${HTTP_SRC})

target_compile_options(${LIB_MOVENIU_HTTP}
    PUBLIC -std=c++11 
    PUBLIC -DASIO_STANDALONE
    PUBLIC -D${OS_NAME}
)
