First, login to your VM using `ssh abid@IP`

- Step 1: Download Anaconda
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
 this should print `/home/abid/anaconda3/bin/python` if anaconda is installed and activated successfully
