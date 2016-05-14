project( ImGui )

file( GLOB HDRS_FILES *.h *.hpp )
file( GLOB SRCS_FILES *.cpp )

add_library( ${PROJECT_NAME} STATIC ${SRCS_FILES} ${HDRS_FILES} )
