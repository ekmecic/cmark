project('cmark', 'c', default_options: ['warning_level=3'])

headers = [
  'src/cmark.h',
  'src/parser.h',
  'src/buffer.h',
  'src/node.h',
  'src/iterator.h',
  'src/chunk.h',
  'src/references.h',
  'src/utf8.h',
  'src/scanners.h',
  'src/inlines.h',
  'src/houdini.h',
  'src/cmark_ctype.h',
  'src/render.h',
  'src/cmark_version.h',
  'src/cmark_export.h',
  'src/config.h',
]

src = [
  'src/cmark.c',
  'src/node.c',
  'src/iterator.c',
  'src/blocks.c',
  'src/inlines.c',
  'src/scanners.c',
  'src/utf8.c',
  'src/buffer.c',
  'src/references.c',
  'src/render.c',
  'src/man.c',
  'src/xml.c',
  'src/html.c',
  'src/commonmark.c',
  'src/latex.c',
  'src/houdini_href_e.c',
  'src/houdini_html_e.c',
  'src/houdini_html_u.c',
  'src/cmark_ctype.c',
]

add_project_arguments('-fvisibility=hidden', language : 'c')
inc = include_directories('src')
cmark_lib = static_library('cmark', src, include_directories : inc)
cmark_dep = declare_dependency(link_with: cmark_lib, include_directories : inc)
