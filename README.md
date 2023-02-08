# Failing Docker container

to test the issue, run the following
```
$ docker build --tag issue-1 .
```

you should see the following error after a minute or two

```
#11 143.8 Gem::Ext::BuildError: ERROR: Failed to build gem native extension.
#11 143.8 
#11 143.8 current directory:
#11 143.8 /opt/ruby/lib/ruby/gems/2.6.0/bundler/gems/http_parser.rb-54b17ba8c7d8/ext/ruby_http_parser
#11 143.8 /opt/ruby/bin/ruby -I /opt/ruby/lib/ruby/2.6.0 -r
#11 143.8 ./siteconf20230208-7-19zjn5v.rb extconf.rb
#11 143.8 *** extconf.rb failed ***
#11 143.8 Could not create Makefile due to some reason, probably lack of necessary
#11 143.8 libraries and/or headers.  Check the mkmf.log file for more details.  You may
#11 143.8 need configuration options.
#11 143.8 
#11 143.8 Provided configuration options:
#11 143.8       --with-opt-dir
#11 143.8       --without-opt-dir
#11 143.8       --with-opt-include
#11 143.8       --without-opt-include=${opt-dir}/include
#11 143.8       --with-opt-lib
#11 143.8       --without-opt-lib=${opt-dir}/lib
#11 143.8       --with-make-prog
#11 143.8       --without-make-prog
#11 143.8       --srcdir=.
#11 143.8       --curdir
#11 143.8       --ruby=/opt/ruby/bin/$(RUBY_BASE_NAME)
#11 143.8 extconf.rb:17:in `read': No such file or directory @ rb_sysopen -
#11 143.8 /opt/ruby/lib/ruby/gems/2.6.0/bundler/gems/http_parser.rb-54b17ba8c7d8/ext/ruby_http_parser/vendor/http-parser/http_parser.c
#11 143.8 (Errno::ENOENT)
#11 143.8       from extconf.rb:17:in `block (2 levels) in <main>'
#11 143.8       from extconf.rb:16:in `open'
#11 143.8       from extconf.rb:16:in `block in <main>'
#11 143.8       from extconf.rb:15:in `each'
#11 143.8       from extconf.rb:15:in `<main>'
#11 143.8 
#11 143.8 extconf failed, exit code 1
#11 143.8 
#11 143.8 Gem files will remain installed in
#11 143.8 /opt/ruby/lib/ruby/gems/2.6.0/bundler/gems/http_parser.rb-54b17ba8c7d8 for
#11 143.8 inspection.
#11 143.8 Results logged to
#11 143.8 /opt/ruby/lib/ruby/gems/2.6.0/bundler/gems/extensions/x86_64-linux/2.6.0-static/http_parser.rb-54b17ba8c7d8/gem_make.out
#11 143.8 
#11 143.8   /opt/ruby/lib/ruby/2.6.0/rubygems/ext/builder.rb:99:in `run'
#11 143.8 /opt/ruby/lib/ruby/2.6.0/rubygems/ext/ext_conf_builder.rb:47:in `block in
#11 143.8 build'
#11 143.8   /opt/ruby/lib/ruby/2.6.0/tempfile.rb:295:in `open'
#11 143.8   /opt/ruby/lib/ruby/2.6.0/rubygems/ext/ext_conf_builder.rb:29:in `build'
#11 143.8 /opt/ruby/lib/ruby/2.6.0/rubygems/ext/builder.rb:185:in `block in
#11 143.8 build_extension'
#11 143.8   /opt/ruby/lib/ruby/2.6.0/monitor.rb:230:in `mon_synchronize'
#11 143.8   /opt/ruby/lib/ruby/2.6.0/rubygems/ext/builder.rb:181:in `build_extension'
#11 143.8 /opt/ruby/lib/ruby/2.6.0/rubygems/ext/builder.rb:229:in `block in
#11 143.8 build_extensions'
#11 143.8   /opt/ruby/lib/ruby/2.6.0/rubygems/ext/builder.rb:226:in `each'
#11 143.8   /opt/ruby/lib/ruby/2.6.0/rubygems/ext/builder.rb:226:in `build_extensions'
#11 143.8   /opt/ruby/lib/ruby/2.6.0/rubygems/installer.rb:813:in `build_extensions'
#11 143.8 /opt/ruby/lib/ruby/gems/2.6.0/gems/bundler-2.4.6/lib/bundler/rubygems_gem_installer.rb:72:in
#11 143.8 `build_extensions'
#11 143.8 /opt/ruby/lib/ruby/gems/2.6.0/gems/bundler-2.4.6/lib/bundler/source/path/installer.rb:28:in
#11 143.8 `post_install'
#11 143.8 /opt/ruby/lib/ruby/gems/2.6.0/gems/bundler-2.4.6/lib/bundler/source/path.rb:244:in
#11 143.8 `generate_bin'
#11 143.8 /opt/ruby/lib/ruby/gems/2.6.0/gems/bundler-2.4.6/lib/bundler/source/git.rb:188:in
#11 143.8 `install'
#11 143.8 /opt/ruby/lib/ruby/gems/2.6.0/gems/bundler-2.4.6/lib/bundler/installer/gem_installer.rb:54:in
#11 143.8 `install'
#11 143.8 /opt/ruby/lib/ruby/gems/2.6.0/gems/bundler-2.4.6/lib/bundler/installer/gem_installer.rb:16:in
#11 143.8 `install_from_spec'
#11 143.8 /opt/ruby/lib/ruby/gems/2.6.0/gems/bundler-2.4.6/lib/bundler/installer/parallel_installer.rb:155:in
#11 143.8 `do_install'
#11 143.8 /opt/ruby/lib/ruby/gems/2.6.0/gems/bundler-2.4.6/lib/bundler/installer/parallel_installer.rb:146:in
#11 143.8 `block in worker_pool'
#11 143.8 /opt/ruby/lib/ruby/gems/2.6.0/gems/bundler-2.4.6/lib/bundler/worker.rb:62:in
#11 143.8 `apply_func'
#11 143.8 /opt/ruby/lib/ruby/gems/2.6.0/gems/bundler-2.4.6/lib/bundler/worker.rb:57:in
#11 143.8 `block in process_queue'
#11 143.8 /opt/ruby/lib/ruby/gems/2.6.0/gems/bundler-2.4.6/lib/bundler/worker.rb:54:in
#11 143.8 `loop'
#11 143.8 /opt/ruby/lib/ruby/gems/2.6.0/gems/bundler-2.4.6/lib/bundler/worker.rb:54:in
#11 143.8 `process_queue'
#11 143.8 /opt/ruby/lib/ruby/gems/2.6.0/gems/bundler-2.4.6/lib/bundler/worker.rb:90:in
#11 143.8 `block (2 levels) in create_threads'
#11 143.8 
#11 143.8 An error occurred while installing http_parser.rb (0.6.1), and Bundler cannot
#11 143.8 continue.
#11 143.8 
#11 143.8 In Gemfile:
#11 143.8   goldfinger was resolved to 2.1.0, which depends on
#11 143.8     http was resolved to 3.3.0, which depends on
#11 143.8       http_parser.rb
------
executor failed running [bash -c cd /opt/tmp-name  &&   bundle install &&       yarn install --pure-lockfile]: exit code: 5
```
