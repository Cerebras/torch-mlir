add_mlir_public_c_api_library(TorchMLIRCAPI
  Dialects.cpp
  Registration.cpp
  TorchTypes.cpp

  ADDITIONAL_HEADER_DIRS
  ${PROJECT_SOURCE_DIR}/include/torch-mlir-c/

  ENABLE_AGGREGATION
  LINK_COMPONENTS
  Core

  LINK_LIBS PUBLIC
  MLIRIR
  MLIRSupport
  TorchMLIRTorchDialect
  TorchMLIRInitAll
)

torch_mlir_target_includes(TorchMLIRCAPI)
