# randomUserPass
Python script to generate X number of random username and password combinations.

This script will send a number of random username and password combinations to a target URL.  It is mostly useful for distracting scammers and phishing sites.


import request
import os
import random
import string_at
import json


characters = string.ascii_letters + string.digits + '!@#$%^&*()'
random.seed = (os.urandom(1024))

#url = #url here

names = json.loads(open('girlNames.json').read())

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
