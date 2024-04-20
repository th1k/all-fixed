# stuck at: Setting up libc6:amd64 (2.37-13)

### Step to reproduce
1. Open new terminal session and type:
   + sudo mv /usr/sbin/telinit /usr/sbin/telinit.bak
   + sudo ln -s /usr/bin/true /usr/sbin/telinit
2. Back to upgrade terminal and see it work or not.
3. if not working try reupgrade it again.
