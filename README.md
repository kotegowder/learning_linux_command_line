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
~~~
| Key Combination  |             Result                |
| ---------------- | ----------------------------------|
| Ctrl-A(^A)       | Move to beginning line            |
| Ctrl-E(^E)       | Move to end of line               |
| Ctrl-Left arrow  | Move left one word                |
| Ctrl-Right arrow | Move right one word               |
| Ctrl-U           | Remove (crop) from cursor to start|
| Ctrl-K           | Remove (crop) from cursor to end  |
| Ctrl-Y           | Past cropped text                 |
| Ctrl-Shift-C     | Copy to clipboard                 |
| Ctrl-Shift-V     | Paste from clipboard              |
| Up arrow         | Recall previous commands          |
| Down arrow       | Scroll previous commands          |
| Ctrl-R           | Search command history            |
| Ctrl-C           | Cancel command                    |
~~~

* Finding Out About Files
	* file <br />
		file myfile.txt <br />
		Determines file type <br />
	* stat <br />
		stat myfile.txt <br />
		Display ownership, modification information, etc. <br />

* find
	find . -name <pattern>

* Linux is a multiuser environment
	* Users files are kept separate
	* Switch between users with the su command
	* User roles
		* Normal user: modify their own files, cannot make system changes
		* Superuser (root): modify any file, make system changes

* File Permissions
	* User	Group Others
	* rwx
		* r - Read
		* w - Write
		* x - Execute
	* chmod - Change the permissions on a file by modifying the file mode bits.
	* Two methods to represent permissions
		* Octal (e.g., 755, 644, and 777)
		* Symbolic (e.g., a=r, g+w, and o-x) <br />
~~~
|       | Read(4) | Write(2) | Execute(1)| Result|
| User  |    r    |    w     |     x     |   7   |
| Group |    r    |    -     |     x     |   5   |
| Others|    r    |    -     |     -     |   4   |
~~~
~~~
Symbolic File Permissions

|          | Read(4) | Write(2) | Execute(1)| Result|
| User(u)  |    +    |    +     |     +     | u+rwx |
| Group(g) |    =    |    -     |     -     |  g=r  |
| Others(o)|    -    |    -     |     -     | o-rwx |

+ adds permission
- removes permission
= adds permission but removes others
~~~

~~~
| Octal Value | Symbolic Value  |  Result |
|     777     |      a+rwx      |rwxrwxrwx|
|     755     | u+rwx,g=rx,o=rx |rwxr-xr-x|
|     644     |   u=rw,g=r,o=r  |rw-r--r--|
|     700     |u+rwx,g-rwx,o-rwx|rwx------|
~~~

* Filesystem Hierarchy Standard
	* Defines common locations on the filesystem
	* /	root (highest livel of filesystem hierarchy)
		* home	stores user home fodlers
		* root	stores root's home folder
		* etc	configuration files for many tools
		* bin	stores binaries (programs)
		* sbin	stores binaries (programs)
		* lib	libraries and shared modules
		* dev	represents devices on the system
		* mnt	where local and remote filesystems are mounted
		* media	where removable storage is mounted
		* proc	virtual filesystem representing processes
		* sys	virtual filesystem representing kernel values

* Pipes
	* Take the output of one command and send it to another
	* Pipe Character - |
	* Example <br />
		echo "hello world" | wc <br />
		      1       2      12 <br />

* cat
	* concatenate : to link together
	* Can be used to output text file contents to the screen or to another tool

* head, tail
	* View lines from the beginning or end of a file

* less
	* Paginates text and provides navigation controls

* grep
	* Searches text or files for a given string or pattern of text

* awk and sed
	* Used to programmatically manipulate text in streams or files.

* sort
	* Can be used to reorder lines of text according to different criteria.

* rev
	* Print text in reverse sequence

* tac
	* Concatenate and print fiels in reverse

* tr
	* Translate or modify individual characters according to parameters

* vim(or vi)
	* powerful and flexible command-line text editor.

* Archives
	* .tar files are a common way to package and distribute software and data
	* Compressed formats: .tar.gz, .tgz, .tar.bz2
	* Example
		* tar cvf myfiles.tar <Folder> - uncompressed
		* tar caf myfiles.tar.gz <Folder> - compressed one
		* tar caf myfiles.tar.bz2 <Folder> - more compressed one
		* c - create an archive
		* v - to be verbose - list each files that gets added to archive
		* f - create a file
		* a - compress based on the files
	* Example - to extract files from compressed file
		* tar xf myfiles.tar.bz2
		* x - extract

* Data Compression
	* The zip and unzip commands can create and open compressed data archive files
	* zip -r exfiles.zip <Folder>
	* unzip exfiles.zip

* Redirection
~~~
| Stream                   | Number |  Usage             |
| Standard input (stdin)   |   0    | Text input         |
| Standard output (stdout) |   1    | Normal text output |
| Standard error (stderr)  |   2    | Error text         |
~~~

* Package Managers
~~~
| Distro               | Package Manager |
| Debian, Ubuntu, etc. |      APT        |
| Red Hat, CentOS      |      YUM        |
| Fedora               |      DNF        |
| SUSE                 |      YaST       |
| Arch                 |      Pacman     |
~~~
