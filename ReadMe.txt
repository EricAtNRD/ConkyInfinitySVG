Installation Instructions for Infinity Theme for Conky

Step 1 : Install Conky
                Ubuntu :   apt-get install conky-all
                Fedora : yum install conky
                see documentation for other distros in order to install conky
Step 2 : Extract the Infinity tar file
Step 3 :  change the name of conkyrc to .conkyrc
                change name of lua to .lua
                change name of conky to .conky
Step 4 : Copy these 3 files .conkyrc, .lua and .conky files to your home directory
                cp * ~/
Step 5 : Open .conkyrc and adjust the screen resolution according to your desktop
Step 6 : Also adjust haunted.lua in .lua directory according to screen resolution
Step 7 : I have  also given u a file named rev-eng.psd in order to modify the background image of conky so u can adjust it too.
Step 8 : Some scripts for mem,cpu etc have been written separately . you can delete them
Step 9 : Now you are ready to run conky
                open terminal and type $chmod a+x ~/.conky/startconky.sh
                                                            $sh ~/.conky/startconky.sh
                                                            it will start after delay of 15
                                                            add this file to startup application in order to load it at startup
            OR
            Run Directly :   $ conky&