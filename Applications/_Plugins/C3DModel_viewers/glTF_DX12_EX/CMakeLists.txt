
add_library(Plugin_C3DModel_Viewers_glTF_DX12_EX)

file(GLOB_RECURSE SRCS

	*.cpp
	*.h
)

target_sources(Plugin_C3DModel_Viewers_glTF_DX12_EX PRIVATE

	${SRCS}
)

target_include_directories(Plugin_C3DModel_Viewers_glTF_DX12_EX PUBLIC

	./
	./media
	./DX12Util
)

target_link_libraries(Plugin_C3DModel_Viewers_glTF_DX12_EX PRIVATE

	CompressonatorLIB

	ExtDirectX
	
	Plugin_Common_D3DX12
	Plugin_GLTF_DX12
	GPU_Decode
	Plugin_CmdLine
	Plugin_Model_Viewer
	Plugin_Common_QtImgui_DX12
	Plugin_Common_Misc
)

set_target_properties(Plugin_C3DModel_Viewers_glTF_DX12_EX PROPERTIES FOLDER ${FOLDER_NAME})
