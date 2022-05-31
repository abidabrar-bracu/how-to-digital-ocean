First, download the `credentials.json` file following [this](https://youtu.be/_HLlLyYwu24) tutorial.


On your local machine, make a zip folder named `cse251_bot_codes` with the following files:
- `quickstart.py`
- `variables.py`
- `google_sheets_code.py`
- `credentials.json`
- `bot_code.py`
- `custom_functions.py`
- `messages_string.py`

Update the variables in the `variables.py` and `messages_string.py` as you did in the previous semesters. In the `variables.py`, keep `dashboard_enabled = False`, therefore, you don't need to change anything from `line 73` and onwards

Also, in the `variables.py`, `SPREADSHEET_ID` is the Google Sheet ID of Enrolment Manager sheet, and `SPREADSHEET_ID_2 = SPREADSHEET_ID_3` is the Google Sheet ID for the marks sheet (use the template [here](https://docs.google.com/spreadsheets/d/1fEFu57ZBTd-K0GrNloiO9o5tMMjPYTKjTwi3JPbYEbg/edit?usp=sharing))

Restart the command prompt, DON'T ssh to VM first. We will first copy the files to our VM using `scp`
```bash
cd Downloads
scp -r path/to/file/cse251_bot_codes abid@IP:~/
```

Now log in to the VM using `ssh abid@IP`. We first need to create a `token.json` file for accessing Google Sheet

```bash
cd cse251_bot_codes/
python quickstart.py
```
Open the link in your browser, select `@bracu.ac.bd` account, click `Allow`, copy the code, paste it in the terminal, and press `Enter`. If no error shows, congratulations!

Now we can start the discord bot!
```bash
tmux
python bot_code.py
```
Wait till `bot is up and running` messages. When running for the first time, it might prompt you for the **Authorization code** similar to the one you had to do when running `quickstart.py`. To exit without shutting down the bot, first press `CNTRL + B`, then `D`.

To check if there is any error or to check output:
```bash
tmux attach
```
To exit without shutting down the bot, first press `CNTRL + B`, then `D`.
