project('web-archives', ['vala', 'c'],
    version : '0.0.3',
    license : 'GPL3+'
)

i18n = import('i18n')
gnome = import('gnome')

prefix = get_option('prefix')
libdir = get_option('libdir')
datadir = get_option('datadir')
localedir = join_paths(prefix, datadir, 'locale')
webextensionsdir = join_paths(prefix, libdir, meson.project_name(), 'web-extensions')

conf = configuration_data()
conf.set_quoted('VERSION', meson.project_version())
conf.set_quoted('GETTEXT_PACKAGE', meson.project_name())
conf.set_quoted('LOCALEDIR', localedir)
conf.set_quoted('WEB_EXTENSIONS_DIRECTORY', webextensionsdir)

gtk_dep = dependency('gtk+-3.0')
kiwix_dep = dependency('kiwix-glib-1.0')
zim_dep = dependency('zim-glib-3.0')
sqlite_dep = dependency('sqlite3')
webkit_dep = dependency('webkit2gtk-4.0')
soup_dep = dependency('libsoup-2.4')
webkit_web_extension_dep = dependency('webkit2gtk-web-extension-4.0')
tracker_dep = dependency('tracker-sparql-2.0')
xml_dep = dependency('libxml-2.0')
isocodes_dep = dependency('libisocodes')

subdir('src')
subdir('data')
subdir('po')
