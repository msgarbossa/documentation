# Deep Sleep

## Save variables to flash

Flash memory has limited write cycles around 10,000.  RTC memory contains a Python dictionary with 64 key/value pairs. The dictionary keys are integers 0-63.  There is also one RTC variable for storing a string.  There isn't a lot of documentation on this.

```
import machine
import ujson
rtc = machine.RTC()
d = {1:'one', 2:'two'}  # Example data to save
rtc.memory(ujson.dumps(d))  # Save in RTC RAM

r = ujson.loads(rtc.memory())  # Restore from RTC RAM
# r == {2: 'two', 1: 'one'}
```
