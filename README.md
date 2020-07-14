# T-Koala

![image1](https://github.com/LilyGO/T-Koala/blob/master/image/T-Koala2.jpg)

![image2](https://github.com/LilyGO/T-Koala/blob/master/image/T-Koalatypec.jpg)



### Unit 1 [Bluetooth](https://github.com/LilyGO/T-Koala/blob/master/Module_test/Bluetooth_test/Bluetooth_test.ino)

Phone pairing to connect to Bluetooth

```c
void setup() {
  Serial.begin(115200);
  SerialBT.begin("ESP32test"); //Bluetooth device name
  Serial.println("The device started, now you can pair it with bluetooth!");
  Serial.println("My name is ESP32test");
}
```
ESP32 Bluetooth name is set by SerialBT.begin()

---

### Uint 2 [Wifi](https://github.com/LilyGO/T-Koala/tree/master/Module_test/Wifi_test_demo)

#### Wifi_scan
Wifi scan serial port information display can connect wifi name and signal strength

```c
 Serial.begin(115200);

    // Set WiFi to station mode and disconnect from an AP if it was previously connected
    WiFi.mode(WIFI_STA);
    WiFi.disconnect();
    delay(100);

    Serial.println("Setup done")
```

#### Wifi_web_sever

By connecting to WiFi, you can generate a web page.

```c
const char* ssid = "TP-LINK-";//Please input your wifi ID
const char* password = "123456";//Please input your wifi password

//Log in with a browser to generate a mac address:
//example:192.168.0.108
digitalWrite(led, 1);
server.send(200, "text/plain", "hello from esp32!");
digitalWrite(led, 0);
```
Log in to 192.168.0.x,The screen will display:"hello from esp32!"

---
