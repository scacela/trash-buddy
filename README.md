# trash-buddy

Trash Buddy is a file that helps you manage the things you typically discard with rm.
Trash Buddy performs an mv command to move the item(s) to a trash folder, and keeps a record of the things you discard in a text file.

In your ${HOME}/.bash_profile, add the following:
<pre>
trash_buddy_path="/&ltpath on your local machine&gt/trashbuddy"
tb()
{
source ${trash_buddy_path} "$@"
}
</pre>

Then run commands with:
<pre>
$ tb &ltarguments&gt
</pre>

The options for command line arguments are as follows:
<pre>
Flags               Description                                                                   Example Usage

-h  | --help        Show options.                                                                 ${command_name} -h
-i  | --info        a. Show deleted items in your record file by name and recovery path.          ${command_name} -i
                    b. Show lines in your record file that contain user-input string.             ${command_name} -i string_a string_b
-t  | --trash-path  Show the path to your trash folder.                                           ${command_name} -t
&ltno flags&gt          Move any file or directory paths that follow to ${trash_parent_dir} with mv.  ${command_name} item_a item_b
</pre>