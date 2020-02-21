# mhwd-kernel

The script is taken from here: https://wiki.manjaro.org/index.php?title=Mhwd-kern.sh. Instructions are written myself.

I do not own the script. Copyright goes to it's authors (Joshua and some more people).

Some screenshots here: https://imgur.com/gallery/7gA7esT.


Usage:
1. Add Manjaro repo.

    1.1. Make a repository mirrorlist file /etc/pacman.d/mirrorlist-manjaro with one or more repository address. 
    
      Address line example:
       
         Server = https://mirror.futureweb.be/manjaro/stable/core/$arch
         
      Manjaro repositories list can be found here: https://repo.manjaro.org/. It might be necessary to use one with updated Stable branch.
       
    1.2. Add following to your /etc/pacman.conf:
    
         [core]
         Include = /etc/pacman.d/mirrorlist-manjaro
2. Run sync-upgrade:

        sudo pacman -Syyu
3. Install Manjaro keyring.

        sudo pacman -S manjaro-keyring
4. Install MHWD.

        sudo pacman -S mhwd
   If you don't want to user the script, finish here. Proceed to using MHWD. Otherwise, continue.
5. Clone this repository and cd into it's folder.

        git clone https://github.com/NightH4nter/mhwd-kernel.git
    
        cd mhwd-kernel
6. Make the script bootable and run it:

        sudo chmod +x mhwd-kern.sh
        sudo ./mhwd-kern.sh
Done!

You may also consider moving the script somewhere and/or making an alias for regular usage.
