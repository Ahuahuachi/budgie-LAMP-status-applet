project('org.ubuntubudgie.applet.hello-world',
        ['vala', 'c'],
        version: '0.1.0',
        meson_version: '>=0.40.0',
        license: 'GPL2')

am_cflags = [
    '-fstack-protector',
    '-pedantic',
    '-Wstrict-prototypes',
    '-Wundef',
    '-Werror-implicit-function-declaration',
    '-Wformat',
    '-Wformat-security',
    '-Werror=format-security',
    '-Wconversion',
    '-Wunused-variable',
    '-Wunreachable-code',
    '-Wall',
    '-W'
]

add_global_arguments(am_cflags, language: 'c')

# Global path variable
prefix = get_option('prefix')
libdir = join_paths(prefix, get_option('libdir'))
datadir = join_paths(prefix, get_option('datadir'))

LOCALE_DIR = join_paths(prefix, get_option('localedir'))

VAPI_DIR = join_paths(meson.source_root(), 
                      'vapi')

PIXMAPS_DIR = join_paths(datadir, 'pixmaps')

LIB_INSTALL_DIR = join_paths(prefix, libdir, 'budgie-desktop', 'plugins', meson.project_name())

message('Installing applet...')

subdir('src')
subdir('po')
subdir('icons')
