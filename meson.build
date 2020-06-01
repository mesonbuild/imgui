project('imgui', 'cpp',
    version: '1.76',
    license: 'MIT',
)

# Folder `examples` is needed, as it includes
# the implementations for different rendering backends and
# context creation APIs
include_dirs = include_directories('.', 'examples')

sources = ['imgui_demo.cpp', 'imgui_draw.cpp', 'imgui_widgets.cpp', 'imgui.cpp']
if get_option('opengl3').enabled()
	sources += 'examples/imgui_impl_opengl3.cpp'
endif
if get_option('dx12').enabled()
	sources += 'examples/imgui_impl_dx12.cpp'
endif
if get_option('dx9').enabled()
	sources += 'examples/imgui_impl_dx9.cpp'
endif
if get_option('opengl2').enabled()
	sources += 'examples/imgui_impl_opengl2.cpp'
endif
if get_option('glut').enabled()
	sources += 'examples/imgui_impl_glut.cpp'
endif
if get_option('dx11').enabled()
	sources += 'examples/imgui_impl_dx11.cpp'
endif
if get_option('win32').enabled()
	sources += 'examples/imgui_impl_win32.cpp'
endif
if get_option('sdl').enabled()
	sources += 'examples/imgui_impl_sdl.cpp'
endif
if get_option('glfw').enabled()
	sources += 'examples/imgui_impl_glfw.cpp'
endif
if get_option('dx10').enabled()
	sources += 'examples/imgui_impl_dx10.cpp'
endif
if get_option('allegro5').enabled()
	sources += 'examples/imgui_impl_allegro5.cpp'
endif
if get_option('vulkan').enabled()
	sources += 'examples/imgui_impl_vulkan.cpp'
endif
if get_option('marmalade').enabled()
	sources += 'examples/imgui_impl_marmalade.cpp'
endif
if get_option('osx').enabled()
	sources += 'examples/imgui_impl_osx.mm'
endif
if get_option('metal').enabled()
	sources += 'examples/imgui_impl_metal.mm'
endif

imgui = library('imgui',
	sources,
	dependencies: [
		# TODO: add other dependencies
		dependency('vulkan', required: get_option('vulkan'))
		dependency('glfw3', required: get_option('glfw'))
		dependency('sdl', required: get_option('sdl'))
		dependency('glut', required: get_option('glut'))
	],
	include_directories: include_dirs
)

imgui_dep = declare_dependency(include_directories: include_dirs, link_with: imgui)
