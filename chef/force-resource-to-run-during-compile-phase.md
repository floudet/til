# Force Resource to Run During Compile Phase

Let's say that in your recipe you want to run a command via Mixlib::ShellOut but the binary you want to execute is provided by a package you need to install first.

Your code will probably look like this:

```ruby
  package 'mybinary' do
    action :install
  end

  run_mybinary = Mixlib::ShellOut.new('/path/to/mybinary --option arg').run_command
  run_mybinary.error!
```

And fail with a variant of "/path/to/mybinary:No such file or directory"

What happened? If you look at the chef-client run logs, you'll notice that the command was executed before the package installation.

Chef uses a two-pass system, first it evaluates all recipes to build the resource collection (compile phase), then it converges each resource (execution phase). Any top-level ruby code happens in the first phase. 

To circumvent this, use `.run_action(:some_action)` at the end of a resource block to force the specified action to run during the compile phase.

Our example above, corrected:
```ruby
  package 'mybinary' do
    action :nothing
  end.run_action(:install)

  run_mybinary = Mixlib::ShellOut.new('/path/to/mybinary --option arg').run_command
  run_mybinary.error!
```

[Source](https://docs.chef.io/resource_common/#run_action)
[More on Chef two-pass model](https://coderanger.net/two-pass)
