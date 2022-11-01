# M17-Image-TRX
Transmitting one base64 encoded image with M17 and SDRAngel via RF

*1 - Convert JPEG to Base64*

The 120 x 120px JPEG [image](PU4THZ_M17_JPG.jpg)

Was converted using [Base64 Guru Website](https://base64.guru/converter/encode/file ) and the output is:

```
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
```

*2 - Transmit with SDRAngel M17 modulator via HackRF on 70cm*

Image was split into 600byte packets and sent via packet mode on 438.5MHz. Deviation is set to 8Khz and Bandwith to 18KHz (maybe some internal conversion of sdrangel ?)

The python code below does the split:

```
test = "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"
[print(test[i:i+600]+"\n") for i in range(0, len(test), 600)]
```

![image](https://user-images.githubusercontent.com/58897843/199345010-be373972-fa88-4761-bbc3-f5d6720ecc2b.png)

*3 - Recieve with SDRAngel M17 demodulator via RTLSDR on 70cm*

Image was recieved via packet mode on 438.5MHz. Deviation is set to 8Khz and Bandwith to 18KHz...

![image](https://user-images.githubusercontent.com/58897843/199345098-c84aa68f-20a1-47f2-a058-926d297bbf61.png)

Base64 Recieved Output:

```
=== 19:06:14 PU4THZ to PU4THZ ===
/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAQEBAQEBAQEBAQGBgUGBggHBwcHCAwJCQkJCQwTDA4MDA4MExEUEA8QFBEeFxUVFx4iHRsdIiolJSo0MjRERFwBBAQEBAQEBAQEBAYGBQYGCAcHBwcIDAkJCQkJDBMMDgwMDgwTERQQDxAUER4XFRUXHiIdGx0iKiUlKjQyNEREXP/CABEIAHgAeAMBIgACEQEDEQH/xAAdAAACAgMBAQEAAAAAAAAAAAAABgQFAwcJAgEI/9oACAEBAAAAAOf4G4UexsrNJbtUAB9N41FtQOFNO0QB1+KCDVKGFfwI2JcxIUDugKteuokBVj6q+KEfWtX3DFatoEKAqYNVChG1pV9xBWraBCgKmDVQoRtaVfcQVq2gQoCpg1UKEbWlX3EFatoEKAqYNVChG1pV9xBWraBCgKmDVQoRtaVfcQVq2gQoCpg1UJ8fWlWxGDovvuLyq1rhge4vuFGgHrq1+nji3qsD778efgdDt4eeZWuAAANlbWQlmRSv1+sWGn64BpvPdKojTfwPqKH/xAAbAQACAgMBAAAAAAAAAAAAAAAACAUGAwQHAf/aAAgB
=== 19:06:24 PU4THZ to PU4THZ ===
/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAQEBAQEBAQEBAQGBgUGBggHBwcHCAwJCQkJCQwTDA4MDA4MExEUEA8QFBEeFxUVFx4iHRsdIiolJSo0MjRERFwBBAQEBAQEBAQEBAYGBQYGCAcHBwcIDAkJCQkJDBMMDgwMDgwTERQQDxAUER4XFRUXHiIdGx0iKiUlKjQyNEREXP/CABEIAHgAeAMBIgACEQEDEQH/xAAdAAACAgMBAQEAAAAAAAAAAAAABgQFAwcJAgEI/9oACAEBAAAAAOf4G4UexsrNJbtUAB9N41FtQOFNO0QB1+KCDVKGFfwI2JcxIUDugKteuokBVj6q+KEfWtX3DFatoEKAqYNVChG1pV9xBWraBCgKmDVQoRtaVfcQVq2gQoCpg1UKEbWlX3EFatoEKAqYNVChG1pV9xBWraBCgKmDVQoRtaVfcQVq2gQoCpg1UJ8fWlWxGDovvuLyq1rhge4vuFGgHrq1+nji3qsD778efgdDt4eeZWuAAANlbWQlmRSv1+sWGn64BpvPdKojTfwPqKH/xAAbAQACAgMBAAAAAAAAAAAAAAAACAUGAwQHAf/aAAgB
=== 19:06:31 PU4THZ to PU4THZ ===
/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAQEBAQEBAQEBAQGBgUGBggHBwcHCAwJCQkJCQwTDA4MDA4MExEUEA8QFBEeFxUVFx4iHRsdIiolJSo0MjRERFwBBAQEBAQEBAQEBAYGBQYGCAcHBwcIDAkJCQkJDBMMDgwMDgwTERQQDxAUER4XFRUXHiIdGx0iKiUlKjQyNEREXP/CABEIAHgAeAMBIgACEQEDEQH/xAAdAAACAgMBAQEAAAAAAAAAAAAABgQFAwcJAgEI/9oACAEBAAAAAOf4G4UexsrNJbtUAB9N41FtQOFNO0QB1+KCDVKGFfwI2JcxIUDugKteuokBVj6q+KEfWtX3DFatoEKAqYNVChG1pV9xBWraBCgKmDVQoRtaVfcQVq2gQoCpg1UKEbWlX3EFatoEKAqYNVChG1pV9xBWraBCgKmDVQoRtaVfcQVq2gQoCpg1UJ8fWlWxGDovvuLyq1rhge4vuFGgHrq1+nji3qsD778efgdDt4eeZWuAAANlbWQlmRSv1+sWGn64BpvPdKojTfwPqKH/xAAbAQACAgMBAAAAAAAAAAAAAAAACAUGAwQHAf/aAAgB
=== 19:06:49 PU4THZ to PU4THZ ===
ABCBDBDBDBBDBDBD
=== 19:07:02 PU4THZ to PU4THZ ===
/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAQEBAQEBAQEBAQGBgUGBggHBwcHCAwJCQkJCQwTDA4MDA4MExEUEA8QFBEeFxUVFx4iHRsdIiolJSo0MjRERFwBBAQEBAQEBAQEBAYGBQYGCAcHBwcIDAkJCQkJDBMMDgwMDgwTERQQDxAUER4XFRUXHiIdGx0iKiUlKjQyNEREXP/CABEIAHgAeAMBIgACEQEDEQH/xAAdAAACAgMBAQEAAAAAAAAAAAAABgQFAwcJAgEI/9oACAEBAAAAAOf4G4UexsrNJbtUAB9N41FtQOFNO0QB1+KCDVKGFfwI2JcxIUDugKteuokBVj6q+KEfWtX3DFatoEKAqYNVChG1pV9xBWraBCgKmDVQoRtaVfcQVq2gQoCpg1UKEbWlX3EFatoEKAqYNVChG1pV9xBWraBCgKmDVQoRtaVfcQVq2gQoCpg1UJ8fWlWxGDovvuLyq1rhge4vuFGgHrq1+nji3qsD778efgdDt4eeZWuAAANlbWQlmRSv1+sWGn64BpvPdKojTfwPqKH/xAAbAQACAgMBAAAAAAAAAAAAAAAACAUGAwQHAf/aAAgB
=== 19:07:22 PU4THZ to PU4THZ ===
AhAAAAAAABUmRib3aMDWJSmrWQPQ7rqOWgaatZA9Cu2o5aBps1cD0K66rkoLH7vmbP5JQoAAAAH/xAAbAQEBAAIDAQAAAAAAAAAAAAAACAYHAgQFA//aAAgBAxAAAAAAe9MOurOrzVU35BkEk6zuq29RSflWQSTrO6rb1FJ+VZBJWs7ptrUUo5S6ny9D0uv0+QAA/8QAUBAAAAQDAwcFCgkHDQAAAAAAAQMEBQACBgcREhATFDEyNHEVICEiQQgWGCM1YpSVo9MXQ1FSVmNzotI3RVdhdZOkJDA2RlVkgZKlsbKzwv/aAAgBAQABPwDmH2fsQrWqnEVTKxqx1SM56VGLYUUgmUOqUtSUn0rSpp/jsGPNYce1cEPFP8joaUXacA8sNYuH2QAuUI7vYYoX0grS1Q00o1CKxwdkbHMm+K8e8JCVAFe2wQ7UtTNPVMLO81Mq5OFobF0q5sbdKzor0hKoLilRyUc343a2vNh0s+Zk1Wu9HtVRrVC1okqHlAVTaUmllFkINP8AE3KTsedzPm4YZ6f5YQ1Wu04A5HawcPtQFcnR3e3xRT1MUE8o3RUoquoEwtzWDivEGNOaQVsFBcOn
=== 19:07:32 PU4THZ to PU4THZ ===
YzMRxspUnV7b5rg59wxcMVXWqREsawYGhoFyIp+ngkqCSdUctLUA1EAZ8eKeU0nYvzeIsQvDrwe2DWVPUYnZXFrLUsTUc2LSXJySNu0vUrQNL0swrOliB93U6wDKOINV6uuKOTvDpia1q+9pY2SRzblwN5uYbm+RArzWkJj/ABKvB8yQzN9UdqYItRWsy+o2xbT5c4JgYKfkG9YUr65LYQAy3lFldJWwZ58owD8lJtutLf0jilmRiNbzpVIZo9Mfn0SsCNu+Q3O/fhurhweaZtKbXeVgTgewpsxobM2tpxxwOyPoAUpJU5nUvmwQ8UO7J6cp2m2h2pWYAvcnScKpZrlC83oLL6VQYy0pXRLiDoNnNwjhmyXDFw5PBZsP+gM/rVd76PBasO+gM/rVd76F3c12NkKOik/9RW+9jwcbHg/qr/HLfew7dz9ZGkSgrSUx/HK/ewNilm+vvXl9MVe8g6xazeRNjCmJQH5dLU+8iayOz8R/o6HpCj8cHWTULJfm6c1hdvKj8cGUNSZt2NsAbguAQUGB/tNHeFSQX3NAfvjfxQfSVOSqRlBtC75MZkBSjBIN8qDp4mQ4NCVOqmSdl8cn
=== 19:07:40 PU4THZ to PU4THZ ===
Ivm5XXeQ4QMP/S13j0D8kBqhdukCA9MHbOQdQwo6VY5HUf5ct4xdldt5DhARUPkvIu3SO0YO2Y7IHVCjfByO+/ruIcx23kOEBFQ+SxyLt0jtGDtmOyB1Qo3ybI77+u4hzHbeQ4QEVD5LHIu3SO0YO2Y7IHVCjfJsjvv67iHMdt5DhARUPksci7dI7Rg7ZjsgdUKN8myO+/ruIcx23kOEBFQ+SxyLt0jtGDtmOyB1Qo3ybI77+u4hzHbeQ4QADFQ+SxyL90jtg7VHZA6oUb4OR239dxDJ8ONrH6QX/wBKj4cbWP0gv/pUDbTawdrrx29Jjua3ZbVdlre81E4zLnEXRcGeP2oNbkikLlKKWaJqeaB/NxIcJQi1iuauarR66ZEVRKyG8h2UhKRAWi1h9I1/70YntBrObVUasOE4xJV9RhrdTx4jA1hUI/nM7/MMd8bx/aJ0T1E7zBvpwcJxgV6s3bWj/iIxp6r5/M7kj8jjb+1l8BeI6oGWLavyq2gft5d/yyDAZLhgbvmRw5vc9W32Z0HZsip2ral0BwBYqm3FUf8A9JceFLYd9Pp/VS73MeF
```

*4 - Convert Base64 to BMP again*

Used  ![Base64 Guru Website](https://base64.guru/converter/decode/file) to decode.

Headers were removed and the data joined uing notepad++ steps below:

1 - replace ```^=== 19.*``` with regular expression turned on.
2 - replace ```\r\n``` with regular expression turned on.

Website output screenshot:

![image](https://user-images.githubusercontent.com/58897843/199352351-af5faeaa-0946-41e2-a86c-2812b256882f.png)

And it seems ok!

![image](https://user-images.githubusercontent.com/58897843/199352388-f2954ecb-0ce5-4553-a632-777176f16d17.jpg)

Thanks for reading :) 
