---
title: "VDO System"
permalink: /docs/video-system/
excerpt: "ระบบภาพภายในรถ"
last_modified_at: 2023-07-10T17:48:05-04:00
redirect_from:
  - /theme-setup/
toc: true
---

## การจัดวางภาพ

|  ภาพมองเห็นภายในห้องโดยสาร  |  ภาพมองเห็นหน้าผู้ป่วย  |
|---|---|
|  Bodycam  |  สัญญาณชีพ  |

![vdo layout](/eto-doc/assets/img/vdo-layout.png)

การจัดวางจะวางออกเป็น 4 จอตามตัวอย่าง โดยในวิธีที่ผู้วิจัยได้ใช้คือ ใช้ระบบของอุปกรณ์ NVR ที่เรียกว่า `Channel zero` ทำการรวมภาพ 4 จอ ออกมาเป็นจอภาพเดียว แล้วนำต่อเข้ากับอุปกณ์ Video encoder แล้วให้ Output ออก `/live/0` 1080p H.264 Bitrate 1 Mbps

## การเชื่อมต่อเพื่อดึงสัญญาณภาพ

สามารถทดสอบการเชื่อมต่อได้ด้วย VLC `rtsp://192.xxx.xxx.6/live/0`

![vlc Media > Open Network Stream](/eto-doc/assets/img/vlc-1.png)  
![vlc Open Media](/eto-doc/assets/img/vlc-2.png)  
![vlc example video stream](/eto-doc/assets/img/vlc-example.png)