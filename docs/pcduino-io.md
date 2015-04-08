<!--remove-start-->

# Led Blink on pcDuino3


Example using Johnny-Five + pcDuino-IO to directly control a pcDuino3



More info: [https://github.com/rwaldron/pcduino-io/](https://github.com/rwaldron/pcduino-io/)


Run with:
```bash
node eg/pcduino-io.js
```

<!--remove-end-->

```javascript
var five = require("johnny-five");
var pcDuino = require("pcduino-io");
var board = new five.Board({
  io: new pcDuino()
});

board.on("ready", function() {
  var led = new five.Led(13);
  led.blink();
});


```


## Illustrations / Photos


### pcDuino3



![docs/images/pcduino.jpg](images/pcduino.jpg)  





## Additional Notes


In order to use the pcduino-io library, you will need to install node (0.10.x or better)
and npm on your pcduino. Once the environment is created, install Johnny-Five and pcDuino-IO.

[Setup environment](https://github.com/rwaldron/pcduino-io#install-a-compatible-version-of-nodenpm)

```sh
npm install johnny-five pcduino-io
```





&nbsp;

<!--remove-start-->

## License
Copyright (c) 2012, 2013, 2014 Rick Waldron <waldron.rick@gmail.com>
Licensed under the MIT license.
Copyright (c) 2014, 2015 The Johnny-Five Contributors
Licensed under the MIT license.

<!--remove-end-->