## My server/console/rake task does not run!

### Did you run bundle?
   After adding gems to your Gemfile, did you run ``bundle`` or ``bundle install`` in the terminal?

   **Hint:**

   If trying to run ``rails``, ``rake`` or ``bundle check`` gives you the error message ``Your Gemfile's dependencies could
   not be satisified``, you should run ``bundle`` or ``bundle install`` again and pay attention to eventual error messages.
   Those error messages might either help you find the problem yourself, or if in doubt, ask a coach.

### Did you run all migrations?

   If the error is something like "... has no field _xy_" or "wrong datatype" or "Migrations pending" or anything
   similar, you should try to run ``rake db:migrate``. If this doesn't resolve the problem (or shows error messages like
   "Table _XY_ already exists", you might want to run ``rake db:migrate:reset`` or ``rake db:drop && rake db:create &&
   rake db:migrate`` to re-initialize your workspace.
