# Examples of STR2STR

## Original Heading Sensor

```
# Configure hardware serial port
stty -F /dev/ttySC0 clocal raw speed 38400

# Get RTCM3 from RTK2GO and send to Ardusimple
$HOMEPATH/rtklib/str2str/str2str -in ntripcli://:@rtk2go.com/Umricam -out serial://ttySC0:38400:8:n:1
```

## SNIP in AWS

```
# Configure hardware serial port
stty -F /dev/ttySC0 clocal raw speed 38400

# Get RTCM3 from RTK2GO and send to Ardusimple
$HOMEPATH/rtklib/str2str/str2str -in ntripcli://myrover:12345@ec2-54-78-11-21.eu-west-1.compute.amazonaws.com:2101/BCEP00BKG0 -out serial://ttyS0:115200:8:n:1
```

<figure><img src=".gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

## Connect to RTK2GO post JAN24

```
./str2str -in ntripcli://john.oraw@iotech.ie:@rtk2go.com/Umricam:2101
```
