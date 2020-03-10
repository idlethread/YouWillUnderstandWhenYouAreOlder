
I keep hearing about school closings and wonder how I can "encourage" my son and daughter to spend a little less time on social media and more time learning during school hours if their middle school closes.

Original post on reddit..
https://www.reddit.com/r/pihole/comments/fg5fht/how_to_encourage_your_children_to_use_the/

With the awesome per client features of Pi-hole 5.0 beta it will now be possible to add the ability to periodically block sites and unlock them after points are earned on khan academy, typing club or any site that has a web scrapable point system.

Goal:  After 2 hours, block 2 or 3 sites that my 13 year old uses the most.  Unblock those sites once they have earned 1 point on Typing Club or Khan Academy.

I will update this readme as I do this tonight. 

https://github.com/1stOctet/YouWillUnderstandWhenYouAreOlder

Setup
- Create an account on typing club or khan academy as a parent. Do not use a LINKED facebook or LINKED google account to log in. 

- For this to work you need to create an "old school" email login. This is important because we will have a nodejs script that will log in as you to check your child's account for points.

- Todo (Explain how to install Linux on a raspberry pi or old computer)

- Todo (Explain how to install pi-hole and upgrade to pi-hole 5.0 beta)

- sudo apt install nodejs npm git

- npm i puppeteer

- npm i get-stdin

- git clone https://github.com/1stOctet/YouWillUnderstandWhenYouAreOlder.git

Currently using this guide https://github.com/pi-hole/docs/blob/release/v5.0/docs/database/gravity/example.md
to understand how to flip a site from blocked to not blocked via the "Raw database instructions"

Look at database-script1.sh first before running. Trust but verify.
- sudo bash database-script1.sh 

- Todo (Explain how to figure out what your child's ip address is using the pi-hole web interface)

Please first modify the database-script2.sh file and change 222.222.222.222 ip to your child's ip address.
- sudo bash database-script2.sh 

Look at database-script3.sh first before running. Trust but verify.
- sudo bash database-script3.sh 

Please first modify the database-script3.sh to include the domains you want to block.
- sudo bash database-script4.sh 

This script is unecessary if you use the pi-hole web interface to link the domains to a group.
If it doesn't make sense to you, please use the pi-hole gui.
Be sure to edit this file for the number of domains you are blocking periodically to ensure your child goes to Harvard.
- sudo bash database-script5.sh 

