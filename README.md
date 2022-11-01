# M17-Image-TRX
Transmitting one base64 encoded image with M17 and SDRAngel via RF

*1 - Convert 4-BIT BMP to Base64 using*

The 41 x 10px 4Bit Bitmap [download pu4thz_bmp.zip](https://github.com/Paulo-D2000/M17-Image-TRX/files/9914092/pu4thz_bmp.zip

Preview:

[image](https://user-images.githubusercontent.com/58897843/199344811-d042aa5f-44ee-498f-aa40-fdadb04a2a4a.png)

Was converted using [Base64 Guru Website](https://base64.guru/converter/encode/file ) and the output is:

```
Qk1oAQAAAAAAAHYAAAAoAAAAKQAAAAoAAAABAAQAAAAAAPIAAAASCwAAEgsAAAAAAAAAAAAAAAAAABEREQAiIiIAMzMzAERERABVVVUAZmZmAHd3dwCIiIgAmZmZAKqqqgC7u7sAzMzMAN3d3QDu7u4A////AP//////////////////////////8AAAev//////////////////////////8vH////w///wAAD//w//8P/w//D/AAAP8QX////w///w//D//w//8P/w//D/D///8QD/8P/wAADw//D/AAD/8P/wAAD/8P//8wD/8P/w//Dw//D/Dw//8P/w//D//wD/8AD/8P/w//Dw//D/D///8P/w//D///8P+JH/8P/wAADw//D/D//wAADw//D/AAAP9AL/8P//////////////////////////8gD/8P//////////////////////////8AD//wAA
```

*2 - Transmit with SDRAngel M17 modulator via HackRF on 70cm*

Image was sent via packet mode on 438.5MHz. Deviation is set to 8Khz and Bandwith to 18KHz (maybe some internal conversion of sdrangel ?)

![image](https://user-images.githubusercontent.com/58897843/199345010-be373972-fa88-4761-bbc3-f5d6720ecc2b.png)

*3 - Recieve with SDRAngel M17 demodulator via RTLSDR on 70cm*

Image was recieved via packet mode on 438.5MHz. Deviation is set to 8Khz and Bandwith to 18KHz...

![image](https://user-images.githubusercontent.com/58897843/199345098-c84aa68f-20a1-47f2-a058-926d297bbf61.png)

Base64 Recieved Output:

```
=== 18:27:10 PU4THZ to PU4THZ ===
Qk1oAQAAAAAAAHYAAAAoAAAAKQAAAAoAAAABAAQAAAAAAPIAAAASCwAAEgsAAAAAAAAAAAAAAAAAABEREQAiIiIAMzMzAERERABVVVUAZmZmAHd3dwCIiIgAmZmZAKqqqgC7u7sAzMzMAN3d3QDu7u4A////AP//////////////////////////8AAAev//////////////////////////8vH////w///wAAD//w//8P/w//D/AAAP8QX////w///w//D//w//8P/w//D/D///8QD/8P/wAADw//D/AAD/8P/wAAD/8P//8wD/8P/w//Dw//D/Dw//8P/w//D//wD/8AD/8P/w//Dw//D/D///8P/w//D///8P+JH/8P/wAADw//D/D//wAADw//D/AAAP9AL/8P//////////////////////////8gD/8P//////////////////////////8AD//wAA
```

*4 - Convert Base64 to BMP again*

Used  ![Base64 Guru Website](https://base64.guru/converter/decode/file) to decode, dont forget to remove the "=== 18:27:10 PU4THZ to PU4THZ ===" header...

Website output screenshot:

![image](https://user-images.githubusercontent.com/58897843/199346104-b7e51e0a-b379-419d-a741-9d81df0d2e26.png)

And it seems ok!

![image](https://user-images.githubusercontent.com/58897843/199346201-8df7ba20-bf67-43c6-802b-b0ddcc6b82d8.png)

Downloaded file: [image.zip](https://github.com/Paulo-D2000/M17-Image-TRX/files/9914120/image.zip)

Thanks for reading :) 
