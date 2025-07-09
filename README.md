# test_setup_ruby

Diagnosing a ruby/setup-ruby issue.

## Commands used to create this project

Using Ruby 2.7.8

```bash
# Rails install required manually installing certain gem versions and retrying
gem install rails -v 6.0.6.1
# Use older concurrent-ruby
# See: https://stackoverflow.com/questions/79360526/uninitialized-constant-activesupportloggerthreadsafelevellogger-nameerror#answer-79507723
gem install concurrent-ruby -v 1.3.4
gem uninstall concurrent-ruby -v 1.3.5
rails _6.0.6.1_ new test_setup_ruby
cd test_setup_ruby/
gem update --system 3.4.22
# Add `gem 'concurrent-ruby', '1.3.4'` to Gemfile
bin/setup
```
