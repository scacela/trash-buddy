# trash-buddy

In your ${HOME}/.bash_profile, add the following:
<pre>
trash_buddy_path="/<path to trashbuddy>/trashbuddy"
tb()
{
source ${trash_buddy_path} "$@"
}
</pre>

Then run commands with:
<pre>
$ tb <arguments>
</pre>

The options for command line arguments are as follows:
<pre>
Flags               Description                                                                   Example Usage

-h  | --help        Show options.                                                                 ${command_name} -h
-i  | --info        a. Show deleted items in your record file by name and recovery path.          ${command_name} -i
                    b. Show lines in your record file that contain user-input string.             ${command_name} -i string_a string_b
-t  | --trash-path  Show the path to your trash folder.                                           ${command_name} -t
<no flags>          Move any file or directory paths that follow to ${trash_parent_dir} with mv.  ${command_name} item_a item_b
</pre>