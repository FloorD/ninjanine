## IT DOES NOT WORK

### Have you checked...?

Don't panic, there might be an easy explanation and solution for your current problem.

Please run through the check list with us:

### My changes do not show!

1. [Did you save your changes?](cheatsheet/changes.md#did-you-save-your-changes)

2. [Did you restart the server?](cheatsheet/changes.md#did-you-restart-the-server)

### My server/console/rake task does not run!

1. [Did you run ``bundle``?](cheatsheet/bundler.md#did-you-run-bundle)
2. [Did you run all migrations?](cheatsheet/bundler.md#did-you-run-all-migrations)

   If the error is something like "... has no field _xy_" or "wrong datatype" or "Migrations pending" or anything
   similar, you should try to run ``rake db:migrate``. If this doesn't resolve the problem (or shows error messages like
   "Table _XY_ already exists", you might want to run ``rake db:migrate:reset`` or ``rake db:drop && rake db:create &&
   rake db:migrate`` to re-initialize your workspace.

### There's that ugly error instead of my page!

1. Did you check for typos in your code?

   There's various reasons why rails code won't run. If the message contains 'Syntax Error', then Most likely it's
   because you have a missing closing parenthesis ``)`` or curly brace ``}``

   If the message contains 'nil has no function' or 'would output the object id of nil', then you might have mistyped a
   variable name (e.g. omitting the ``@`` for member variables of simple letter swpa (see what I did there?) is
   responsible). Correct the error, save the file, and in case the error doesn't go away, restart the server. If that
   doesn't solve your problem - ask a coach.



###Bonus: are you using Rails 4?
Run ```rails -v``` in your terminal to figure out which version of Rails you are using. It helps you Google your error messages, plus: a few problems with the Rails Girls (follow-up) guides are related to the Rails version you're using. Make sure to tell your coach what version you're running!

###Handling error messages

1. Take a deep breath

2. Scroll up (there's a thing called a 'stack trace', and usually only the first lines are interesting. As an example:

```
SyntaxError - /.../app/controllers/welcome_controller.rb:3: unterminated string meets end of file
/.../app/controllers/welcome_controller.rb:3: syntax error, unexpected end-of-input, expecting keyword_end:
  app/controllers/welcome_controller.rb:3:in `'
  activesupport (4.0.0) lib/active_support/dependencies.rb:423:in `block in load_file'
  activesupport (4.0.0) lib/active_support/dependencies.rb:615:in `new_constants_in'
  activesupport (4.0.0) lib/active_support/dependencies.rb:422:in `load_file'
  activesupport (4.0.0) lib/active_support/dependencies.rb:323:in `require_or_load'
  activesupport (4.0.0) lib/active_support/dependencies.rb:462:in `load_missing_constant'
  activesupport (4.0.0) lib/active_support/dependencies.rb:183:in `const_missing'
  activesupport (4.0.0) lib/active_support/inflector/methods.rb:226:in `block in constantize'
  activesupport (4.0.0) lib/active_support/inflector/methods.rb:224:in `constantize...

...
```

Here the first line shows me that the problem is in the controller 'welcome_controller', in the method 'index' on line
'3'. I would then:

   1. Open the file and see if there is a problem with that line (in that case, I forgot to close a simple ``'`` quote),
      correct the problem, save the file and check again

   2. Copy the error to my browser and google for it.

      Most problems have been discovered by others. There's usually a good discussion at 'stackoverflow' about it. Check
      for the answers with the highest votes and people with the best overall reputation, and you will most likely find
      an answer. Others appear at ruby or rails forums, or even in the rails guides. If everything fails, ask a colleague.

   3. Ask your coach for help.
