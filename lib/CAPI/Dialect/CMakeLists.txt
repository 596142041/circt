# TODO: Make the check source feature optional as an argument on *_add_library.
set(LLVM_OPTIONAL_SOURCES
  Comb.cpp
  ESI.cpp
  RTL.cpp
  SV.cpp
)

add_circt_library(CIRCTCAPIComb

  Comb.cpp

  ADDITIONAL_HEADER_DIRS
  ${MLIR_MAIN_INCLUDE_DIR}/mlir-c

  LINK_LIBS PUBLIC
  MLIRCAPIIR
  CIRCTComb
  )

add_circt_library(CIRCTCAPIESI

  ESI.cpp

  ADDITIONAL_HEADER_DIRS
  ${MLIR_MAIN_INCLUDE_DIR}/mlir-c

  LINK_LIBS PUBLIC
  MLIRCAPIIR
  CIRCTESI
  )

add_circt_library(CIRCTCAPIRTL

  RTL.cpp

  ADDITIONAL_HEADER_DIRS
  ${MLIR_MAIN_INCLUDE_DIR}/mlir-c

  LINK_LIBS PUBLIC
  MLIRCAPIIR
  CIRCTRTL
  )

add_circt_library(CIRCTCAPISV

  SV.cpp

  ADDITIONAL_HEADER_DIRS
  ${MLIR_MAIN_INCLUDE_DIR}/mlir-c

  LINK_LIBS PUBLIC
  MLIRCAPIIR
  CIRCTSV
  CIRCTSVTransforms
  )
