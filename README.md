The command setting specifies the program to run; in this case that is g++.exe. The args array specifies the command-line arguments that will be passed to g++. These arguments must be specified in the order expected by the compiler. You are telling g++ on WSL to grab the source file in our current workspace directory on Windows, compile it, then place the executable file in our helloworld folder under the $HOME/projects/helloworld folder in WSL.

The label value is what you will see in the VS Code Command Palette; you can name this whatever you like.

The isDefault": true value in the group object specifies that this task will be run when you press Ctrl+Shift+B. This property is for convenience only; if you set it to false you'll have to run it from the Command Palette menu under Tasks: Run Build Task.

The windows.options.shell setting tells VS Code to use the WSL Bash shell to run the commands that are defined in this file. If you set the default terminal to WSL globally in the earlier step in this tutorial, then you can remove the windows setting here.