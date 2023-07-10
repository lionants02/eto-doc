---
layout: splash
permalink: /
hidden: true
header:
  image: /assets/img/banner.png
---
<div align="center">
  <pre class="mermaid">
    mindmap
    root((ETO<br/>Gateway))
        ระบบภาพภายในรถ
        ::icon(fa fa-ambulance)
            กล้อง<br/>ภาพรวม
            ::icon(fa fa-camera)
            กล้อง<br/>หน้าผู้ป่วย
            ::icon(fa fa-camera)
            Body camera<br/>ไร้สาย
            ::icon(fa fa-camera)
            ภาพจาก<br/>based site monitor
            ::icon(fa fa-heartbeat)
            
        Vender<br/>broker
            Based site monitor
            ::icon(fa fa-heartbeat)
            12 lead ecg
            ::icon(fa fa-heartbeat)

        Panel Pc
        ::icon(fa fa-tablet)
            Mic
            ::icon(fa fa-microphone)
            Speaker
            ::icon(fa fa-volume-up)
            Software
                D1669 Medinfo
        Fingerprint
        ::icon(fa fa-hand)
        Wifi Hotspot
        ::icon(fa fa-wifi)
        
  </pre>
</div>

![อุปกรณ์ ETO](/eto-doc/assets/img/eto-device.png)
![web api](/eto-doc/assets/img/eto-web-api.png)