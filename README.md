
## The Game - Presentation & First Iteration

You sell Travel Insurance. You get requests for quotes, and you reply with quotes (prices). When you give the right quote, you win cash.

YOU RECEIVE

	POST /quote HTTP/1.1
	{
	  "country":"PL",
	  "departureDate":"2016-11-15",
	  "returnDate":"2016-12-09",
	  "travellerAges":[32,39],
	  "options":["MedicalConditions"],
	  "cover":"Basic"
	}

YOU REPLY

	200

	{
	  ”quote": 234.5
	}

YOU ALSO RECEIVE

	POST /feedback HTTP/1.1
	{
	   "message": ”Congrats Cyriux: …”
		”type" : WIN | LOOSE | ERROR
	}

## Implementation

Use your FAVORITE REST stack

Otherwise you may start from bootstrap here: https://github.com/dlresende/extreme-carpaccio) & choose your language in /client. But BEWARE: Please ADAPT /order to /quote & Order -> Request and feedback.content to feedback.message)

Make it work:

- Dev Environment
- Http POST handling: /quote & /feedback
- Json parsing
- Dates handling
… ...then score points already!

## Register your server

Connect to the game server (server IP to be given)

In the top little form, fill-in your team name, your password (to prevent other from usurpating your score), and your public IP:port. You can register again using the same name and passwor when you wish.

![Registration form](/registration.png)

Once you are registered, your team becomes listed in the score board.

![The score board on the game server](/scoreboard.png)

**REMEMBER: THE GAME SERVER IS RIGHT EVEN WHEN IT’S WRONG**

## The calculation

	QUOTE = 1.8
		x 	NB DAYS
		x 	NB TRAVELERS
	where 
		NB DAYS = 
		return date - departure date

**This calculation will change in the next iterations**. You may want to create some tests to help change later...

## Troubleshouting

- Use Postman to test your server

**!!!You Are Not Ready Until You Get Requests on Your /feedback!!!**

