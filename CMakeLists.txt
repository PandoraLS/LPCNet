cmake_minimum_required(VERSION 3.16)
project(lpcnet_demo C)

set(CMAKE_C_STANDARD 11)

include_directories(include)
include_directories(src)

add_executable(lpcnet_demo
        include/lpcnet.h
        src/_kiss_fft_guts.h
        src/arch.h
        src/celt_lpc.c
        src/celt_lpc.h
        src/ceps_codebooks.c
        src/common.c
        src/common.h
        src/freq.c
        src/freq.h
        src/kiss99.c
        src/kiss99.h
        src/kiss_fft.c
        src/kiss_fft.h
        src/lpcnet.c
        src/lpcnet_dec.c
        src/lpcnet_enc.c
        src/lpcnet_plc.c
        src/lpcnet_demo.c
        src/lpcnet_private.h
        src/nnet.c
        src/nnet.h
        src/nnet_data.c
        src/nnet_data.h
        src/opus_types.h
        src/pitch.c
        src/pitch.h
        src/tansig_table.h
        src/vec.h
        src/vec_avx.h
        src/vec_neon.h)

target_link_libraries(lpcnet_demo m)