# Instagram dictionary attack

**NOTE:** For educational puposes only, I do not take credit for any harm, that has been done with this software.

This is a dictionary attack for instagram, using Python.


***You will need to install some modules for the scripts to run:***

 ```pip install selenium ```
 
 ```pip install stem  ```
 
 
 ***You also have to have a chromedriver downloaded for this to work***
 
 
 **Before starting the script you will need to edit two lines in the code, which indicates the directory that your chromedriver is in.**
 
 
 ```python 
 driver = webdriver.Chrome(options=options, executable_path=r'C:/webdrivers/chromedriver.exe')
 ```
 
 ^^ Here, change "C:/webdrivers/chromedriver.exe"  to your directory.  Do this twice at **line 87 and 117.**
 
 
 
 **Keep it in mind, that you have to have TOR configured for this.**
 
 **You have to have port 9050 and 9051 opened and used by TOR**
 
 
 For port 9051 to work, you have to change the **torrc** file.
 
 Find this part in the file:
 ```
 ## The port on which Tor will listen for local connections from Tor
## controller applications, as documented in control-spec.txt.
# ControlPort 9051
## If you enable the controlport, be sure to enable one of these
## authentication methods, to prevent attackers from accessing it.
# HashedControlPassword (Your hashed password will be here)
# CookieAuthentication 1
 ```
 
 **NOW uncomment the following (remove the # sign)**
 
 ```
 # ControlPort 9051
# CookieAuthentication 1
 ```
 
 **SAVE the file**, and start up TOR.
 
 ```tor.exe -f torrc```
 
 **NOTE** In your password file, remove any passwords that are less than 6 characters, as Instagram does not let you to click the button if the password is less than 6 characters.   -- (I'll make it work later).
 
 ***USAGE of the script***
 
 ```py insta.py [-u] [-pl]```

```-u : The username of the victim```
  
```-pl : The passwordlist to be used```

