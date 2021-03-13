# pi-to-microbit-bluetooth

## Micro:bit setup
Create a hex file from the microbit.py file or drag and drop the attached hex file on to the micro:bit. You must have flashed the microbit before proceeding.

Once complete put the micro:bit into pairing mode by holding the two buttons and pressing the reset, release the reset, release the button when the bluetooth logo appears.

## Raspberry Pi Setup

From a terminal window type:
```
bluetoothctl
```

Then enable device scanning by entering:

```
scan on
```

You should see the micro:bit like this:

```
Device XX:XX:XX:XX:XX:XX BBC micro:bit
```

Copy and save the device address XX:XX:XX:XX:XX:XX somewhere.

Then disable device scanning by entering:

```
scan off
```

To pair with the micro:bit type:
```
  pair XX:XX:XX:XX:XX:XX
```

You will be prompted to confirm that you want to pair the device, type:

```
yes
```

Once paired the micro:bit will restart. 

Once it has restarted you can connect to the device with:

```
connect XX:XX:XX:XX:XX:XX
```

You should see it connect and display a message saying 'Pi Connected' followed by a raspberry pi logo.

To disconnect from the micro:bit type:

```
disconnect XX:XX:XX:XX:XX:XX
```

**If you flash the micro:bit again in the future you will have to remove the device and pair again**

To remove the device enter bluetoothctl again and type:

```
remove XX:XX:XX:XX:XX:XX
```

