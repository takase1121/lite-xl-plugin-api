project('lite_xl_plugin_api', 'c', 'cpp', version: 'v0.0.1')

inc = include_directories('include')

cc = meson.get_compiler('c')
lua_version_num = cc.compute_int('LUA_VERSION_NUM',
                                  prefix: '#include "lite_xl_plugin_api.h"',
                                  include_directories: inc)
lite_xl_plugin_api_dep = declare_dependency(include_directories: inc,
                                            variables: { 'lua_version_num': lua_version_num.to_string() })
