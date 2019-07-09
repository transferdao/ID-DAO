# IdentityDAO User Flow Mockups:

## Table of Contents

1. Currently Implemented GoodDollar Flow
2. Prospective Flow
3. Inspiration/Research on Signup/Identity Verification Flows
     * Coinbase
     * 3Box
     * Alchemy


## Currently Implemented GoodDollar Flow:

* Create a wallet ---> Enter details (Full Name) ----> Phone verification
* Login ---> Enter seed phrase ---> Main app page (landing) 


## Prospective Flow:

* Create a wallet ---> Enter details (Full Name, Email) AND account verification text boxes (Facebook/LinkedIn/Twitter [ Verify (button)* ]) ---> Approval sent!** 

/* Mini-flow of [ Verify ] ---> Instructions page ---> (in new tab) Path for doing on-platform verifying (such as tweeting a unique code) ---> Enter details page
** Send email confirming approval sending, and give seed phrase. At this point, the user has an account on GoodDollar, simply not approved (and can access approval status in this way)





## Inspiration/Research on Signup/Identity Verification Flows:

* Looking at currently existing flows can allow us to reap some of the advantages of the conventional UI/UX principles that are likely integrated into these mass-used webapps
* 3box, Coinbase, Peepeth, (Portis?)




### Coinbase:

Sign Up --> Create your account
-First name
-Last name
-Email
-Password
-State
[ ](By continuing I certify that I am 18 years of age, and I agree to the User Agreement and Privacy Policy.)
[ Create Account (button)]
---> Verify your email

(Loading circle around email icon)
(We sent a verification email to EMAIL. Click the link inside to get started!)

(Email didn't arrive?)
(Go back to coinbase.com) (Note, this is outside the center div, more as a "footer")

----> Phone Number Verification


Add your phone number

Country
[ (Flag) United States ] (dropdown)

Your Phone Number
[ 123 - 456 - 7890 ]

This will secure your account by testing a short confirmation code to your phone when logging in.

[ Send code (button)]
(Go back to coinbase.com) (Note, this is outside the center div, more as a "footer")

||| ON CLICK, NEW CENTER DIV |||
Please enter the seven digit code we just send to your number +x xxx xxx xx02 (displays last two digits on number, rest redacted by xs)

[ Chat icon ] [ 0 0 0 0 0 0 0 ]

Didn't receive the SMS? Re-send SMS
Use another phone number

[ Submit ]


----> Identity Verification


Verify your identity

New York state financial regulations require us to verify your identity. Once complete, you can buy, sell or transfer cryptocurrency.

-First name
-Last name
-What will you use Coinbase for? (dropdown)
-Date of birth (three dropdowns)
-What is your source of funds?
-Street Address
-Current Occupation
-Employer
-Last 4 digits of SSN

[ Continue (button) ]

----> Landing page

...

Within Dashboard, we eventually run into need to verify identity, which brings up this modal:

Identity Verification Requested

Select ID type

[ Driver's License ] [ Photo ID ]

I don't have one of these IDs

||| On clicking an ID type: |||


Choose an upload method

[ Webcam ] [ Mobile Camera ] [ File Upload ]

Go back


( If clicking Webcam: )


Example
[DIV below is on the left, takes up approx. 40% of the space]

(Minimalist image of ID card)

• Turn up your brightness and avoid glare
• First name and last name clearly visible
• Date of birth clearly visible
• ID number clearly visible
• Fully in frame, not cut off on any side

[DIV below is on the right, takes up approx. 60% of the space]

[ Please enable your webcam ] (large gray box)

( If clicking Mobile Camera: )


Upload from your mobile phone

Click the link we just sent to +x xxx xxx xx01 and upload photos of your driver's license
( Loading gif )

Please do not leave this page until you are done uploading.

Go back


( If clicking File Upload: )

Upload images

Upload pictures of your photo id (JPEG or PNG).

[ (icon of window) 
Drag & drop 
or click to 
upload ]
Front

(same as above piece, but for back. Front and back buttons are side-to-side)

Please do not redact, watermark or otherwise obscure any part of your ID. This will help ensure we can verify your identity document as quickly and accurately as possible.

[ Upload (button) ]
Go back


==============================================================================

### 3box

-Login is simply Metamask sign-in + signature requested


Identifying information:
-Basic (Add basic information so others can recognize you.)
  -Name
  -Description
  -Spirit Emoji

-About
  -Location
  -Website or URL
  -Birthday
  -Member Since (auto-filled, simply a constant label)

Contact
  -Email

-Work
  -Employer
  -Job Title

-Education
  -School
  -Degree
  -Major
  -Year

Form for Verified Accounts:

Verified Accounts

Connect your existing social
accounts to build a stronger
reputation.

(above chunk occupies the left)


Enter your handles and without the @ mark.

Github  [       Verify(link/button) ]
Twitter [       Verify(link/button) ]



=> On click Github verify:

----------
NEW MODAL
----------

Verify your Github account

Linking your Github account to your 3box profile allows youir friends and apps to trust you more.
 
(below 3 steps are in columns)

1

Copy your unique key below.

[key in box here]

[Click to copy (button)]


2

Open a new gist file in Github
and paste the key in the body of the file.
Save the gist as public with any
valid name and file type.

[Open a gist file (button)] ---> https://gist.github.com/ (Create a new Gist)

3

Check if your Github account was successfully verified below!

(In a blue box)
[ Github not yet verified / Your Github is verified! ]

[ Verify (button) ] (on click --> check Github gists)



[ Done (button) ]


----------------
OUT OF MODAL
----------------

Github [ EMAIL (check icon)       Remove(link/button)]



=> On click Twitter

NEW MODAL:

[Twitter icon] Verify your Twitter account
Linking your Twitter account to your 3Box profile allows your friends and
apps to trust you more.


1

Tweet a unique key from the account you want to
connect

[ _______ ]


[ Tweet this (button) ]


2

Check if your Twitter account was successfully verified below!

[ Twitter not yet verified / Your Twitter is verified! ]

[ Verify (button) ]


  => On Tweet this button:

Twitter opened:
"What's happening?"

[ (Textbox)

This tweet links my 3Box profile to my twitter account! 

Join web3's social profiles network by creating your account on http://3box.io/ today. 
@3boxdb

✅    
did:muport:________________________________________       
✅ 

]

============================================================================

### Alchemy

Identity Verification:



[ Image ]
(Image on a left div)

Name:
[                  ]

Description:
[

                   ]

Social Verification

(Twitter Icon)*
(GitHub icon)


(Warning icon) Prove it's you by linking your social accounts

Authenticate your identity by linking your social accounts. Once
linked, your social accounts will display in your profile page, and
server as proof that you are who you say you are.



Rep. Score:
___ % Rep.

Gen:
___

-
ETH:
+_

ETH Address:
0x__________________


*on click of Twitter icon:
   -If not signed in, Twitter popup "Authorize DAOstack Alchemy to use your account? ... This application will be able to: -Read Tweets from your timeline ... -Post Tweets for you. Will not be able to: ..."
   -(Make a Tweet! (Autofilled with text))