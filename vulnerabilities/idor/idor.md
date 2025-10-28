# IDOR (Insecure Direct Object Reference)

these are my personal notes and understanding of IDOR  
writing this in simplest way so i can revise later and not forget

## what is idor?

- accessing stuff you are not supposed to see or edit  
- just by changing some id or file name in url  
- no hacking tools needed, just logic + guess

## example

www.spinshop.com/user_id=1323  
↓ change it to  
www.spinshop.com/user_id=1322

if it shows someone else’s account = idor

another one:

www.spinshop.com/id=123&file=/database/coffee.png  
↓ change file  
www.spinshop.com/id=123&file=/database/tee.png

if it loads another file = idor exists

## why this happens?

- server only checks if user is logged in  
- but it does not check if the data actually belongs to that user  
- ids are simple like 1, 2, 3 → easy to guess  
- only frontend check, no backend validation

## risk / impact

- can view or edit someone else’s data  
- profile info, orders, invoices, images, etc  
- sometimes can even act like admin  
- big privacy issue

## how to prevent it

- always check on server-side: “does this user own this data?”  
- don’t trust url parameters blindly  
- use random / unguessable ids (UUIDs) instead of 123,124…  
- return 403 (forbidden) or 404 (not found) if someone tries to access others data  
- don’t allow direct file paths from user input  
- add logging and rate limit so people can’t keep guessing ids

## summary in one line

idor = you change some id in url → get access to other people’s data → because backend didn’t check ownership.  
this is super common on websites with /user?id=... or /file=... type urls.  
easy to find, high impact, and easily preventable if backend does proper access control.
