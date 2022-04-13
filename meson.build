project(
  'arm-memhook',
  'c',
  version : '2.34.9',
  meson_version : '>=0.47.0',
)

if host_machine.cpu_family() != 'arm'
  error('Only support arm platform!')
endif

src = ['memcpy_impl.S', 'memmove.S']

add_project_arguments('-include', 'extra.h', language : 'c')

shared_library(
  'arm-memhook',
  src,
  version : meson.project_version(),
  install : true,
)

static_library(
  'arm-memhook',
  src,
  install : true,
)
