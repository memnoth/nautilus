tests = [
  ['test-file-utilities-get-common-filename-prefix', [
    'test-file-utilities-get-common-filename-prefix.c'
  ]],
  ['test-eel-string-get-common-prefix', [
    'test-eel-string-get-common-prefix.c'
  ]],
  ['test-file-utilities', [
    'test-file-utilities.c'
  ]],
  ['test-file-operations-dir-has-files', [
    'test-file-operations-dir-has-files.c'
  ]]
]

foreach t: tests
  test(
    t[0],
    executable(t[0], t[1], dependencies: libnautilus_dep),
    env: [
      test_env,
      'G_TEST_BUILDDIR=@0@'.format(meson.current_build_dir()),
      'G_TEST_SRCDIR=@0@'.format(meson.current_source_dir())
    ]
  )
endforeach
