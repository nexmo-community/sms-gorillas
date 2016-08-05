BrowserGORILLAS.BAS
===================
This is a fork adding SMS control to the excellent JavaScript implementation of the classic [GORILLAS.BAS](http://en.wikipedia.org/wiki/Gorillas_%28video_game%29) found here: http://theraccoonshare.com/GORILLAS.BAS

Don't judge. There be hackyness here.

## How it Works (the SMS part)
This little hack uses Nexmo to receive SMS message controlling the gorillas, and PubNub to push those the commands to the browser. The only restriction is a single player (as determined by their phone number) can not play twice in a row.

This means a game can certainly be hijacked by another player. That's on you. Be nice.

## Setup
Deploy this fantastic code on a server someplace, and make sure you run `composer install` to bring in all the dependencies. 

You'll need both a Nexmo account, and a PubNub account - and their associated credentials. Rename the `config.json.dist` file to `config.json` and add your Nexmo and PubNub credentials.

Once that's setup, you'll need to head to the Nexmo dashboard and point a phone number's SMS webhook to `/public/sms.php`.

Once that's done, pull up the app in a browser, and start sending it SMS.
