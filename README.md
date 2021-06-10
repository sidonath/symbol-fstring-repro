# README

Steps to reproduce:

* Check out f80612b34b9a02da53e5dadf4faeb45956a09cfe
* Attempt to boot Rails with any command (e.g. `rails r "puts 'Works'"`)
* The Rails boots successfully
* Check out `main` HEAD
* Attempt to boot Rails with any command (e.g. `rails r "puts 'Works'"`)
* Rails does not boot and produces an error:

```
$ rails r "puts 'Works'"                                                                                                                                                                             -- INSERT --
/home/.rbenv/versions/2.7.1/lib/ruby/gems/2.7.0/gems/activesupport-6.1.3.2/lib/active_support/dependencies.rb:332:in `require': cannot load such file -- fstring/fstring (LoadError)
        from /home/.rbenv/versions/2.7.1/lib/ruby/gems/2.7.0/gems/activesupport-6.1.3.2/lib/active_support/dependencies.rb:332:in `block in require'
        from /home/.rbenv/versions/2.7.1/lib/ruby/gems/2.7.0/gems/activesupport-6.1.3.2/lib/active_support/dependencies.rb:299:in `load_dependency'
        from /home/.rbenv/versions/2.7.1/lib/ruby/gems/2.7.0/gems/activesupport-6.1.3.2/lib/active_support/dependencies.rb:332:in `require'
        from /home/.rbenv/versions/2.7.1/lib/ruby/gems/2.7.0/gems/symbol-fstring-1.0.1/lib/fstring.rb:6:in `<module:FString>'
        from /home/.rbenv/versions/2.7.1/lib/ruby/gems/2.7.0/gems/symbol-fstring-1.0.1/lib/fstring.rb:5:in `<top (required)>'
        from /home/.rbenv/versions/2.7.1/lib/ruby/gems/2.7.0/gems/activesupport-6.1.3.2/lib/active_support/dependencies.rb:332:in `require'
        from /home/.rbenv/versions/2.7.1/lib/ruby/gems/2.7.0/gems/activesupport-6.1.3.2/lib/active_support/dependencies.rb:332:in `block in require'
        from /home/.rbenv/versions/2.7.1/lib/ruby/gems/2.7.0/gems/activesupport-6.1.3.2/lib/active_support/dependencies.rb:299:in `load_dependency'
        from /home/.rbenv/versions/2.7.1/lib/ruby/gems/2.7.0/gems/activesupport-6.1.3.2/lib/active_support/dependencies.rb:332:in `require'
        from /home/.rbenv/versions/2.7.1/lib/ruby/gems/2.7.0/gems/symbol-fstring-1.0.1/lib/symbol-fstring.rb:3:in `<top (required)>'
        from /home/.rbenv/versions/2.7.1/lib/ruby/2.7.0/bundler/runtime.rb:74:in `require'
        from /home/.rbenv/versions/2.7.1/lib/ruby/2.7.0/bundler/runtime.rb:74:in `block (2 levels) in require'
        from /home/.rbenv/versions/2.7.1/lib/ruby/2.7.0/bundler/runtime.rb:69:in `each'
        from /home/.rbenv/versions/2.7.1/lib/ruby/2.7.0/bundler/runtime.rb:69:in `block in require'
        from /home/.rbenv/versions/2.7.1/lib/ruby/2.7.0/bundler/runtime.rb:58:in `each'
        from /home/.rbenv/versions/2.7.1/lib/ruby/2.7.0/bundler/runtime.rb:58:in `require'
        from /home/.rbenv/versions/2.7.1/lib/ruby/2.7.0/bundler.rb:174:in `require'
        from /home/rails/symbol-fstring-repro/config/application.rb:7:in `<top (required)>'
        from /home/.rbenv/versions/2.7.1/lib/ruby/gems/2.7.0/gems/spring-2.1.1/lib/spring/application.rb:92:in `require'
        from /home/.rbenv/versions/2.7.1/lib/ruby/gems/2.7.0/gems/spring-2.1.1/lib/spring/application.rb:92:in `preload'
        from /home/.rbenv/versions/2.7.1/lib/ruby/gems/2.7.0/gems/spring-2.1.1/lib/spring/application.rb:157:in `serve'
        from /home/.rbenv/versions/2.7.1/lib/ruby/gems/2.7.0/gems/spring-2.1.1/lib/spring/application.rb:145:in `block in run'
        from /home/.rbenv/versions/2.7.1/lib/ruby/gems/2.7.0/gems/spring-2.1.1/lib/spring/application.rb:139:in `loop'
        from /home/.rbenv/versions/2.7.1/lib/ruby/gems/2.7.0/gems/spring-2.1.1/lib/spring/application.rb:139:in `run'
        from /home/.rbenv/versions/2.7.1/lib/ruby/gems/2.7.0/gems/spring-2.1.1/lib/spring/application/boot.rb:19:in `<top (required)>'
        from /home/.rbenv/versions/2.7.1/lib/ruby/2.7.0/rubygems/core_ext/kernel_require.rb:72:in `require'
        from /home/.rbenv/versions/2.7.1/lib/ruby/2.7.0/rubygems/core_ext/kernel_require.rb:72:in `require'
        from -e:1:in `<main>'
```
