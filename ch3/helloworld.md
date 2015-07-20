# Hello World

The hello world application for NodeBots is the customary blink of a LED.

## Requirements

1. NodeJS
2. Particle Core Device Id
3. Particle Core User Access Token

## Getting started

On your particle core bread board take a led red or green and place the long end into the `D7` and the short end into the `GND` slot of the breadboard.

Then create a folder on your computer called `jf-helloworld` and cd into that folder.

Enter the following commands:

```
# init as an npm project - default through the prompts
npm init -y
npm install johnny-five --save
npm install spark-io --save
```

Create a file called `index.js`

``` js
var Spark = require('spark-io')
var five = require('johnny-five')

var board = new five.Board({
  io: new Spark({
    token: process.env.SPARK_TOKEN,
    deviceId: process.env.SPARK_DEVICE_ID
  })
})

board.on('ready', function() {
  var led = new five.Led("D7")
  led.blink()
})
```

Finally setup your deviceId and access token as `env` variables:

```
export SPARK_TOKEN=[access token]
export SPARK_DEVICE_ID=[device id]
```

Now you are ready to run you app:

``` sh
node index.js
```

!!! Congrats you should see a LED Blink !!!

[ctrl-c] will close the app.
