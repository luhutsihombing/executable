script executable terminal di Linux untuk copy file atau folder from one remote to another server
dengan passing password
1. apt-get install expect (install expect)<br/>
  Expect scripting language is used to feed input automatically to an interactive program.
  <br/><br/>
2. Buat file dengan remote.sh
3. edit remote.sh<br/><br/>
#!/usr/bin/expect -f<br/>
spawn scp -r root@192.168.90.20:/home/testingcopy5 /home/bmitest1<br/>
expect "assword:"<br/>
send "Pradipta2020\r"<br/>
interact<br/>
<br/><br/>
4. run remote.sh (di terminal ketikan(path dan nama file tersebut) .../remote.sh
<br/><br/>
sangat cocok di integrasikan dengan script java atau php untuk buat scheduler backup data server
