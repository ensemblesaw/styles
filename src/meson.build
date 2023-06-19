conf_data = configuration_data ()
conf_data.set_quoted('STYLEDIR', join_paths (get_option ('prefix'), get_option ('datadir'), meson.project_name(), 'StyleFiles'))

config_header = configure_file (
    input: 'Config.vala.in',
    output: 'Config.vala',
    configuration: conf_data
)

sources = files (
    'StyleRepository.vala'
)
