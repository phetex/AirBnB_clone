0x00. AirBnB clone - The console
The Cmd class provides a simple framework for writing line-oriented command interpreters. These are often useful for test harnesses, administrative tools, and prototypes that will later be wrapped in a more sophisticated interface.

class cmd.Cmd(completekey='tab', stdin=None, stdout=None)
A Cmd instance or subclass instance is a line-oriented interpreter framework. There is no good reason to instantiate Cmd itself; rather, it’s useful as a superclass of an interpreter class you define yourself in order to inherit Cmd’s methods and encapsulate action methods.

The optional argument completekey is the readline name of a completion key; it defaults to Tab. If completekey is not None and readline is available, command completion is done automatically.

The optional arguments stdin and stdout specify the input and output file objects that the Cmd instance or subclass instance will use for input and output. If not specified, they will default to sys.stdin and sys.stdout.

If you want a given stdin to be used, make sure to set the instance’s use_rawinput attribute to False, otherwise stdin will be ignored.

Cmd Objects
A Cmd instance has the following methods:

Cmd.cmdloop(intro=None)
Repeatedly issue a prompt, accept input, parse an initial prefix off the received input, and dispatch to action methods, passing them the remainder of the line as argument.

The optional argument is a banner or intro string to be issued before the first prompt (this overrides the intro class attribute).

If the readline module is loaded, input will automatically inherit bash-like history-list editing (e.g. Control-P scrolls back to the last command, Control-N forward to the next one, Control-F moves the cursor to the right non-destructively, Control-B moves the cursor to the left non-destructively, etc.).
