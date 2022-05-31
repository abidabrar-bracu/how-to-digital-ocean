First, login to your VM using `ssh abid@IP`

 ```bash
 wget https://repo.anaconda.com/archive/Anaconda3-2022.05-Linux-x86_64.sh
 bash Anaconda3-2022.05-Linux-x86_64.sh
 ```
 
 Press `ENTER`, then press `space` to skim through the user agreement. At the end, type `yes` and press `ENTER` **_twice_**.
 
 After installation complete, type `yes`, and to initialize conda.
 
 ```
 . .bashrc
 which python
 ```
 this should print `/home/abid/anaconda3/bin/python` if anaconda is installed and activated successfully.
 ```
 python3 -m pip install -U "discord.py[voice]"
 pip install --upgrade google-api-python-client google-auth-httplib2 google-auth-oauthlib
 ```
The last line might give an error message, ignore for now.
