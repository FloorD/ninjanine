## My changes do not show!

### Did you save your changes?

   Most editors use a combination of Control-S (Command-S) or you can use File&rarr;Save from the menu.

### Did you restart the server?

   First: Stop the server. Find the Terminal you started the server in and press 'CTRL-C'.

   If you find yourself on the command prompt, cool. If not, try pressing 'CTRL-Q', then 'CTRL-C'. If in doubt, ask the
   next coach.

   Second: Start the server using ``rails s`` or ``rails server``.

### Are you working in the correct directory?

On the commandline, it's easy to get lost. Don't worry, we'll get you there. Let's check that step by step:

1. Check the directory of the server:
   Change to the terminal, stop the server (unless it's not running) and use the command ``pwd`` (end with _ENTER_) - it
   should show you the path like this:

   ```bash

   $ pwd
   /Users/you/projects/railsgirls
   ```

   _Attention_: Don't type the ``$`` sign, it just marks the end of the so-called 'prompt', where you are supposed to
   type a command.

2. Check the directory of the files:
   Go to menu __File__&rarr;__Open Recent__. The upper half of the menu should show recently opened and saved files, the
   lower half recently opened directories. It should look about like this:

   ```
   ~/projects/railsgirls/app/controllers/welcome_controller.rb
   ~/railsgirls/app/controllers/welcome_controller.rb
   ...
   ~/projects/railsgirls
   ~/railsgirls
   ```

   _Attention_: The ``~`` sign stands for '/Users/(yourusername)'

   Now, let's bring the things together:

   The easiest thing is to change the server to the correct directory. Let's assume you found out that the files you
   changed are in the directory ``~/railsgirls``. Open your terminal again and type:

   ```bash

   $ cd ~/railsgirls
   $

   ```

   You should be in the correct directory now. Test it:

   ```bash

   $ pwd
   /Users/you/railsgirls
   ```

   Now start the server again:

   ```bash

   $ rails s
   ...

   ```

   Your changes should now show.

### Oh my, I have changes everywhere!

Honestly, the best thing is to ask a coach if they can help you to merge the changes from both directories, and
eliminate one. If you know how to do it yourself - all the better! But it's quite advanced operations for a mere cheat
sheet. So, please ask!

