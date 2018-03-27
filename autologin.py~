from selenium import webdriver
# The Keys class provide keys in the keyboard like RETURN, F1, ALT etc.
from selenium.webdriver.common.keys import Keys

from pyvirtualdisplay import Display
from selenium import webdriver
import sys

import time

#input user name and password for login
user_name = "mk"
password = "qwerty"

# Wait for 5 seconds

# display = Display(visible=0, size=(800, 600))
# display.start()


# here, a instance of Firefox WebDriver is created. You can do it for various browsers
driver = webdriver.Firefox()
driver.set_window_size(100,100)
# The driver.get method will navigate to a page given by the URL.

# before returning control to your test or script.

#print "count ",len(sys.argv)
if len(sys.argv) > 1:
	driver.get("https://172.20.0.1/auth1.html")
	print "im here"
else:
	driver.get("https://172.17.0.1/auth1.html")

# This is used to confirm that the webpage is the right one
assert "Sonic" in driver.title
# we use the 'name' tag to get a handle to the username and password  this finds the appropriate box.
user = driver.find_element_by_name("userName")
passwd = driver.find_element_by_name("pwd")
# use the 'send_keys' function to set the "box's" values to your password and username
user.send_keys(user_name)
passwd.send_keys(password)
# we sumbit the form
passwd.send_keys(Keys.RETURN)
# driver.stop_client()
# we close the window after logging in, the popup which takes care of the 3 hour windows remains open.
 # seconds
time.sleep(5)

driver.close()
# driver.quit()

# driver.quit()
#
# display.stop()
