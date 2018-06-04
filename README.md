script executable terminal di Linux untuk copy file atau folder from one remote to another server
dengan passing password
1. apt-get install expect (install expect)<br/>
  Expect scripting language is used to feed input automatically to an interactive program.
  <br/><br/>
2. Buat file dengan remote.sh
3. edit remote.sh<br/><br/>
#!/usr/bin/expect -f<br/>
spawn scp -r root@192.168.X.X:/home/testingcopy5 /home<br/>
expect "assword:"<br/>
send "yourpassword\r"<br/>
interact<br/>
<br/><br/>
4. run remote.sh (di terminal ketikan(path dan nama file tersebut) .../remote.sh
<br/><br/>
sangat cocok di integrasikan dengan script java atau php untuk buat scheduler backup data server
<br/><br/><br/>
sumber:<br/>
http://www.forummikrotik.com/scripting-%40-mikrotik/10955-tanya-script-executable-terminal-di-ubuntu.html<br/>
https://www.unix.com/unix-for-advanced-and-expert-users/140958-automated-scp-script-passing-password-preserve-source-file-timestamp.html<br/>
https://stackoverflow.com/questions/41396750/using-expect-to-copy-a-file-from-one-remote-to-another<br/>
https://stackoverflow.com/questions/7568738/can-the-expect-script-continue-to-execute-other-command-after-interact?rq=1<br/>
https://www.thegeekstuff.com/2010/10/expect-examples<br/>
http://www.aldo-expert.com/writers/remote-ssh-langsung-login-linux.html<br/>
