Welcome to the World Wide Web
=============================

[:globe_with_meridians: Go to course navigation :globe_with_meridians:](../navigation.md)

A website is a program that receives requests and sends responses over the Internet. But that's a lot easier said than done. Fortunately, it's also so utterly fundamental that the heavy lifting is already done for us by something else; something we call a **web framework**. Most programming languages have a number of web frameworks to choose from and Ruby is no exception. Today we are going to use a framework called [Sinatra :link:](http://www.sinatrarb.com/).

Creating the server
------------------
Create a file in your workspace called `server.rb`

Open the file in the editor and add the following content:

```ruby
require 'sinatra' 
set :bind, '0.0.0.0'
set :port, 3000

get '/' do
  'Hello World!'
end
```

Make sure you save the file. Now try running it from the command line:

```
$ ruby server.rb
```

Your should get an error:

```
/usr/local/rvm/rubies/ruby-2.3.0/lib/ruby/2.3.0/rubygems/core_ext/kernel_require.rb:55:in `require': cannot load such file -- sinatra (LoadError)
from /usr/local/rvm/rubies/ruby-2.3.0/lib/ruby/2.3.0/rubygems/core_ext/kernel_require.rb:55:in `require'
from server.rb:1:in `<main>'
```

That was just to get you warmed up! Error messages often look unfriendly, but they're really rather useful when you get to know them. What does this one mean?

If you throw your hands up in the air and exclaim 'How the devil should I know?', then don't worry. That's how we all feel sometimes. One of the skills of a good developer is to make and test small hypotheses about the cause of an error message, then iterate over the process until the solution is found. Oh, and Google it. You can always just Google it.

But don't spend too long climbing down that rabbit hole, you might never make it back. The answer here is actually much simpler than you might infer from some of the answers on Google. Sinatra is just another Ruby program; but it's not yet installed in our workspace. To install Sinatra, enter the following on the command-line.
```
$ gem install sinatra
```

You should see a few lines of output and a confirmation that a certain number of gems have been installed. Sinatra is itself dependent on some other programs, so when you install Sinatra, those dependencies are installed too.

Lets try running it again:

```
$ ruby server.rb
```

Your program should now be running and sending output to the command line. As a slight diversion the line `set :port, 3000` has told our application to run on the port that is reserved for [Hyper Text Transfer Protocol Secure (HTTPS)](https://en.wikipedia.org/wiki/HTTPS). This means that if you now open another tab in your browser you can now visit your application using it's public `https` url which should look like the following:

`https://[application name, in our case prototypeWebsite]-[Your username].codeanyapp.com`

You can also find url specifiec on the information page that opened when you first started your container on CodeAnywhere. More excitingly: that's a real, live URL. Try opening it from another window, or from your phone. Cool, huh?

To stop the program running at any time, press `Ctrl + C` in the command window.

:twisted_rightwards_arrows: Now that we've completed another small step it's time to switch over again!

Task 1
------

- [ ] Now the gloves come off...a little. Expanding on what we've just done try to create a route called `'/names'` that, when visited, returns both of your names.

------

[:arrow_backward: Previous page](./section1.md) | [Continue to the answers :arrow_forward:](../tasks/task1.md)
