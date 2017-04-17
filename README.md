# OnePlusTwo

## Mailinator Exploit (no longer working)
Context, Part 1:

https://medium.com/@JakeCooper/how-i-hacked-the-oneplus-reservation-system-120ea1a7ad82

### Python (MailinatorExploit.py)
Steps to use :

1. Fill in ```RESERVATIONID``` and ```APITOKEN``` at line 8-9
2. Download and install Requests (http://docs.python-requests.org/en/latest/)
3. Run! (`python MailinatorExploit.py`)

### Javascript (mailinator.js)                                                  
1)Fill in ```RESERVATIONID``` at line 7
2)Fill in ```APITOKEN```` at line 8
3)Run the app using the command
      node mailinator.js


## Gmail Exploit (no longer working)
Context, Part 2:

https://medium.com/@JakeCooper/so-nice-i-did-it-twice-hacking-the-oneplus-reservation-system-again-2e8226c45f9a

### Method 1

1. Fill in ```gmailAddress``` and ```inviteToken``` at line 9-10
2. Run! (`python GmailExploit.py`)
3. Click links in your gmail inbox (or add a python script to automate this)

### Method 2
1. Download and install Requests (http://docs.python-requests.org/en/latest/)
2. Run GmailExploit2.py
3. Enter your email WITH @gmail.com when prompted.
4. Enter your referral code (5-6 digits found on the end of your referral link)
5. Run EmailParser.py
6. Enter your email WITH @gmail.com.
7. Enter your password

Note: EmailParser.py won't work if you have 2-step authentication ON. For the time being, disable it and then run it

### Method 3
    Note: You will need to enable GMAIL API:

    - follow the instruction from https://developers.google.com/gmail/api/quickstart/python

    - just save the client_secret.json on the same directory you are going to run the script

1. Run! (`python GmailExploit3.py send_invites {your gmail address} {invite token} {cache_buster} [--dryrun]`)

      \* [--dryrun] allow you to see the list of emails the invite will send to

2. Wait until you received the email invites. Run! (`python GmailExploit3.py process_invites`)


## GuerrillaMail Exploit (no longer working)

Steps to use:

1. Fill in ```INVITE_TOKEN``` at line 9
2. (Optional) Change how long do you want to wait for the email to arrive ```EMAIL_CHECK_TIMEOUT``` at line 10
3. Download and install Requests (http://docs.python-requests.org/en/latest/)
4. Run! (`python GuerrillaMailExploit.py`)

## Additional Components

### gmailClicker - OnePlusTwo
Click on the confirmation link in a gmail message

Steps to use :

1. Insert your email adress and your password (line 38)
2. Install pip if it is not all done
3. Install request package -> pip install requests 
4. run it 

### EmailParser
Parses emails and curls the confirmation link automatically.

1. Run EmailParser.py
2. Enter your email
3. Enter your password.

### Bruteforce
tries to bruteforce the Oneplus invite system.

Steps to use:
1. replace `email1` with your email and `password` with your password. this is used to claim the invite.
2. replace `email2` with another (or the same) email. this is the email where the invites will be sent.
3. run invite_bruteforce.py
