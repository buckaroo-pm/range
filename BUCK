load('//:buckaroo_macros.bzl', 'buckaroo_deps')
load('//:subdir_glob.bzl', 'subdir_glob')

cxx_library(
  name = 'range',
  header_namespace = '',
  exported_headers = subdir_glob([
    ('', 'tc/**/*.h'),
  ]),
  srcs = glob([
    'tc/**/*.cpp',
  ]),
  deps = buckaroo_deps(),
  visibility = [
    'PUBLIC',
  ],
)

cxx_binary(
  name = 'example',
  srcs = [
    'range.example.cpp',
  ],
  deps = [
    ':range',
  ],
)
