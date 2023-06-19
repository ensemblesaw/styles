project (
    'com.github.ensemblesaw.enstl',
    'c', 'vala',
    version: '0.1.0',
)

# Install accompaniment styles
install_subdir (
    'StyleFiles',
    install_dir: join_paths (get_option ('datadir'), meson.project_name ())
)

subdir ('src')

dependencies = [
    dependency ('glib-2.0')
]

# Define library
libenstl = static_library (
    'enstl-' + meson.project_version().split('.')[0],
    sources,
    config_header,
    dependencies: dependencies,
    install: true,
    install_dir: [true, true, true]
)

enstl_dep = declare_dependency (
    dependencies: dependencies,
    include_directories: include_directories('.'),
    link_with: libenstl
)
