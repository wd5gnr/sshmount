Call like ssh, e.g.,

    sshmount myremotehost # add any ssh options you like

1. It checks for a directory under ~/remote that matches the remote host name (e.g., lab). If it fails to find it, it prints an error message and continues to execute ssh.
2. If the directory exists, the script examines the list of mounted file systems to see if it is already mounted. If it is, the script just continues with ssh.
3. If the directory is not mounted, the script calls sshfs and then proceeds with ssh.

If you link the script to sshunmount, it will unmount the mount from #3 and not log in.

