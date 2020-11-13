# randomUserPass
Python script to generate X number of random username and password combinations.

Adapted from https://www.youtube.com/watch?v=UtNYzv8gLbs.  Check out Engineer Man on the YouTubes.  He's awesome!

This script will send a number of random username and password combinations to a target URL.  It is mostly useful for distracting scammers and phishing sites.


import request
import os
import random
import string_at
import json


characters = string.ascii_letters + string.digits + '!@#$%^&*()'
random.seed = (os.urandom(1024))

#phishing login page url
url = #url here

# you will need to create a names .json file
#format names: "jason",
names = json.loads(open('girlNames.json').read())

# for loop to create names/passwords plus a random value
for name in names:
	name_extra = ''.join(random.choice(string.digits))
	
	username = name.lower() + name_extra + '@yahoo.com'
	password = ''.join(random.choice(chars) for i in range(8))
	
	requests.post(url, allow_redirects=False, data={
		
		'auid2yjauysd2uasdasdasd': username,
		# Get this from right click>inspect>console>preserve log
		# Put in a uname/pword and submit
		# look in log for these fields #
		'kjauysd6sAJSDhyui2yasd': password
	
	})
