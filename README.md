# dev-setup
A few setup/conf files for vim / tmux / tmuxinator

Some extra set up work: 
- this will require you to compile command-t. To do this: 
First check the ruby version your vim has, as it needs to be the same as the one you're using for your system
```
vim
:ruby puts RUBY_VERSION
```
Take note of the ruby version you have there. If its the same as your default system ruby version `ruby --version`, you're good. 
if not, you'll need to set it before doing the `make` below by using `rvm use <ruby_version_number>`

When that's done, do:
```
cd ./vim/bundle/command-t/ruby/command-t/ext/command-t/
make clean
ruby extconf.rb
make
```

The rest should work out of the box. 
