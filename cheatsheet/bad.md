## Handling error messages

### Take a deep breath

Haaaaaah – hooooooooh...

Better?

### Scroll up

There's a thing called a "stack trace", and **usually only the first lines are interesting**. As an example:

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

Here the first line shows me that the problem is in the controller `welcome_controller`, in the method `index` on line `3`. I would then:

1. **Open the file** and see if there is **a problem with that line** (in that case, I forgot to close a single quote (`'`)), correct the problem, save the file and check again
2. **Copy the error to my browser and google for it**. Most problems have been discovered by others. There's usually a good discussion at 'stackoverflow' about it. Check for the answers with the highest votes and people with the best overall reputation, and you will most likely find an answer. Others appear at Ruby or Rails forums, or even in the Rails Guides. If everything fails, ask a colleague.

### Ask your coach for help!

Really, they're here to help you. If you're not satisified with the explanation (or are intimidated by the coach speaking some weird foreign language in a worse accent), then ask any other coach - they shouldn't be territorial!

