ADD_SUBDIRECTORY(./rtklib)
SET(MY_PROGRAM_NAME RTK)                              #!!!HERE!!!
SET(MAIN_EXE_SOURCE                                   #!!!HERE!!!
${PROJECT_SOURCE_DIR}/include/gnss.h
./rtk_class/main.cpp
./rtk_class/gnss.cpp
)
SET(LIBSET                                            #!!!HERE!!!
rtklib)
ADD_EXECUTABLE(${MY_PROGRAM_NAME} ${MAIN_EXE_SOURCE})
TARGET_LINK_LIBRARIES(${MY_PROGRAM_NAME}        
${LIBSET})                
#============AUTOGENERATE===========
