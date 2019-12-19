# learning_linux_command_line

* A Brief Intro to Linux
	* Originally released by Linus Torvalds in 1991
	* Inspired by MINIX/UNIX
	* Intended to be free of cost and free to modify under GNU General Public License
	* Widespread adoption
	* Often includes tools from GNU Project
	* Distro: specific group fo software and conventions
	* Major distros: Arch, Debian, Red Hat, Slackware
	* Linux Mint, Ubuntu, Kali, etc. from Debian
	* CentOS, Fedora, etc. from Red Hat

* The Bash shell is available on most distros and OSes.

* What is command line?
	* Is a text based interface
	* Send typed commands
	* Display text output
	* The environment used is Shell or interpreter
	* 1971: Thompson shell for UNIX
	* Bash: Bourne-again shell - widely used

* How commands are structured? <br/>
	Command		Option(s)	Argument(s) <br/>
	Examples: <br/>
			* ls -lh /usr/bin <br/>
			* sort -u users.txt <br />
			* grep -i "needle" haystack

* apropos - To help you look up a command by its description rather than its name.

* Bash Shortcuts

         Key Combination  |             Result
	----------------- | ----------------------------------
	  Ctrl-A(^A)      | Move to beginning line
	  Ctrl-E(^E)      | Move to end of line
	  Ctrl-Left arrow | Move left one word
	  Ctrl-Right arrow| Move right one word
	  Ctrl-U          | Remove (crop) from cursor to start
	  Ctrl-K          | Remove (crop) from cursor to end
	  Ctrl-Y          | Past cropped text
	  Ctrl-Shift-C    | Copy to clipboard
	  Ctrl-Shift-V    | Paste from clipboard
	  Up arrow        | Recall previous commands
	  Down arrow      | Scroll previous commands
	  Ctrl-R          | Search command history
	  Ctrl-C          | Cancel command
