# ℹ️ About
ultrax is a simple package make by [UltraX](https://youtube.com/UltraX1), it's simply made to make your coding process faster by some functions
 
<div  align="center">
<p>
<a  href="https://nodei.co/npm/ultrax/"><img  src="https://nodei.co/npm/ultrax.png?downloads=true&stars=true"  alt="NPM info"  /></a>

</p>
</div>

---------
## 🔶 Support
In case you have idea's to improve the package, or maybe you found some bugs or you need help, you can contact us from our [Discord Server](https://discord.gg/Qk6j2fpeat)

------
## 📥 Installation

To install ultrax package all you need is [**Node.js**](https://nodejs.org/en/download/).

Then you can open your application terminal and type there:
```
$ npm install ultrax
```
-----------

## ➡️ Functions

The available functions are:

- [**sleep**](https://www.npmjs.com/package/ultrax#sleep) - Function to set timeouts easily
- [**passGen**](https://www.npmjs.com/package/ultrax#passGen) - Function to create passwords made by words and numbers randomly with specified length
- [**bin**](https://www.npmjs.com/package/ultrax#bin) - This is a way to bin a code.

----

## ➡️ More usages

There is currently only an event called [`inviteJoin`](https://www.npmjs.com/package/ultrax#invite-logger-event) in the package which allows you to get some informations about the invite such as the inviter and how many times it got used.

----

## sleep
sleep is a simple function, where is make it easier and faster to make a timeout in your code.
**Example:**

```js
// Importing the package
const ultrax = require('ultrax')

// Destructure the sleep function from the package
const sleep = ultrax.sleep

// this will log "Start!" once i run the application
console.log('Start!')

// using the package sleep function to set a timeout
sleep(5000) // sleep(milliseconds)

// after the 5 seconds (5000 milliseconds) it will log "5 Seconds passed"
console.log('5 Seconds passed')
```
-----

 ## passGen
this is a simple function that can generate passwords using letters and numbers and the password length is custom so you can change it to any length you want!

**Example:**

```js
// Importing the package
const ultrax = require('ultrax')

// Destructure the passGen function from the package
const passGen = ultrax.passGen

// this will log the randomly generate password in your terminal
console.log(passGen(6)) // passGen(6) that mean it will generate a password from 6 characters.

// you can change it by changing passGen(here will be the length of the password)
```
## Bin
This is a way to bin a code.
```js
// Defining the package
const ultrax = require('ultrax')

// if it's empty it returns a message saying "what do you want to bin?"
if (!args.join(' ')) return message.channel.send('What do you want to bin?');
else {
    // else if everything works fine, we will make a new varible called "bin"
    // it will be used to bin the args.join(' ') also known as the message.content
    const bin = await ultrax.bin(args.join(' '));

    // then here we will send the results!
    message.channel.send('Here i binned the code ' + bin)
}
```
## Invite Logger Event
This event is for logging invite uses. This is same as `guildMemberAdd` event but this is custom event which has invite and inviter in it.
```js
// Defining the package
const ultrax = require("ultrax")

//defining discord
const discord = require('discord.js')

// new discord client
const client = new discord.Client()

// To Get The new event working we need to initilize it by:
ultrax.inviteLogger(client) // put here your discord client
// without above code event won't trigger.

// now below event will work
client.on('inviteJoin', (member, invite, inviter) => {
    console.log(`${member.user.tag} joined using invite code ${invite.code} from ${inviter.tag}. Invite was used ${invite.uses} times since its creation.`)
});
```
-----
