test_env += [
  'G_TEST_BUILDDIR=@0@'.format(meson.current_build_dir()),
  'G_TEST_SRCDIR=@0@'.format(meson.current_source_dir())
]

tests = [
  ['test-nautilus-search-engine', [
    'test-nautilus-search-engine.c'
  ]],
  ['test-nautilus-directory-async', [
    'test-nautilus-directory-async.c'
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
