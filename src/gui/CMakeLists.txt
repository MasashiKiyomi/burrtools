find_package(FLTK REQUIRED)
find_package(PNG REQUIRED)
find_package(OpenGL REQUIRED)

add_definitions(${PNG_DEFINITIONS})

include_directories(${FLTK_INCLUDE_DIR})

set(SOURCES
    BlockList.cpp
    BlockList.h
    Fl_Table.cpp
    Fl_Table.h
    Images.cpp
    Images.h
    LFl_Tile.cpp
    LFl_Tile.h
    Layouter.cpp
    Layouter.h
    WindowWidgets.h
    arcball.cpp
    arcball.h
    assertwindow.cpp
    assertwindow.h
    assmimportwindow.cpp
    assmimportwindow.h
    blocklistgroup.cpp
    blocklistgroup.h
    buttongroup.cpp
    buttongroup.h
    configuration.cpp
    configuration.h
    constraintsgroup.cpp
    constraintsgroup.h
    convertwindow.cpp
    convertwindow.h
    gl2ps.c
    gl2ps.h
    grideditor.cpp
    grideditor.h
    grideditor_0.cpp
    grideditor_0.h
    grideditor_1.cpp
    grideditor_1.h
    grideditor_2.cpp
    grideditor_2.h
    grideditor_3.cpp
    grideditor_3.h
    grideditor_4.cpp
    grideditor_4.h
    gridtypegui.cpp
    gridtypegui.h
    groupseditor.cpp
    groupseditor.h
    guigridtype.cpp
    guigridtype.h
    image.cpp
    image.h
    imageexport.cpp
    imageexport.h
    #main.cpp
    mainwindow.cpp
    mainwindow.h
    movementbrowser.cpp
    movementbrowser.h
    multilinewindow.cpp
    multilinewindow.h
    piececolor.cpp
    piececolor.h
    placementbrowser.cpp
    placementbrowser.h
    resultviewer.cpp
    resultviewer.h
    separator.cpp
    separator.h
    statusline.cpp
    statusline.h
    statuswindow.cpp
    statuswindow.h
    stlexport.cpp
    stlexport.h
    togglebutton.cpp
    togglebutton.h
    tooltabs.cpp
    tooltabs.h
    tr.c
    tr.h
    vectorexportwindow.cpp
    vectorexportwindow.h
    view3dgroup.cpp
    view3dgroup.h
    voxeleditgroup.cpp
    voxeleditgroup.h
    voxelframe.cpp
    voxelframe.h
    )

add_library(gui_lib STATIC ${SOURCES})
target_link_libraries(gui_lib ${FLTK_LIBRARIES})
target_link_libraries(gui_lib ${PNG_LIBRARIES})
target_link_libraries(gui_lib ${OPENGL_glu_LIBRARY})
