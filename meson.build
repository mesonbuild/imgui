project('imgui', 'cpp',
    version: '1.76',
    license: 'MIT'
)

include_dirs = include_directories('.', 'examples')

sources = ['imgui_demo.cpp', 'imgui_draw.cpp', 'imgui_widgets.cpp', 'imgui.cpp']


imgui = library('imgui',
    sources,
    include_directories: include_dirs
)

imgui_dep = declare_dependency(include_directories: include_dirs, link_with: imgui)
