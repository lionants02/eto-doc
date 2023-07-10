---
title: "Quick Guide"
permalink: /docs/quick-guide/
excerpt: "ทำความเข้าใจอย่างรวดเร็ว"
last_modified_at: 2023-07-10T08:48:05-04:00
redirect_from:
  - /theme-setup/
toc: true
---

ภาพระบบ ETO  
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

## อธิบายการทำงานระบบ
  - ETO ทำหน้าที่ในการเป็นสื่อกลางในการเชื่อมต่อเพื่อส่งผ่านข้อมูล ของอุปกรณ์ในรถพยาบาลให้เป็นมาตฐานเดียวกัน โดยมีจุดประสงค์เพื่อแก้ปัญหาการใช้งานระบบ Telemed ให้ใช้งานต่าง ยี่ห้อ(Brand) ได้ ส่งผลให้ การพัฒนาระบบเป็นไปในมาตฐานเดียวกันง่ายต่อการพัฒนาต่อ และ การจัดซื้ออุปกรณ์การแพทย์ในงานระบบ Telemed สะดวกยิ่งขึ้น ไม่ติดข้อกำหนดเรื่องการล๊อคสเปค ที่แต่เดิมต้องใช้ยี่ห้อเดียวกันเท่านั้น
  - ระบบภาพภายในรถ เป็นการรวมภาพ vdo 4 จอเข้าด้วยกันเพื่อลด Brandwidth ปัจจุบันใช้ 1080p Bitrate 1 Mbps เชื่อมต่อระบบด้วย rtsp://192.xxx.xxx.6/live/0 เท่านั้น
    - 192.xxx.xxx.6 หมายเลข ip ของอุปกรณ์ ระบบภาพภายในรถ
  - Vender broket อุปกรณ์ที่พัฒนาโดย บริษัทภายนอก เพื่อแปลงข้อมูลจากอุปกรณ์การแพทย์ ให้เป็นรูปแบบมาตฐาน HL7 เพื่อให้ ETO Gateway ส่งข้อมูลไปยังระบบอื่นต่อไป
  - Wifi Hosport ตัว ETO Gateway สามารถปล่อยสัญญาณ Wifi
    - หากเชื่อมอุปกรณ์ภายนอกด้วย ETO Wifi Hosport ตัวอุปกรณ์จะไม่สามารถเข้าถึง เครือข่ายภายนอกได้ ใช้งานได้เฉพาะภายในวง 192.xxx.xxx.0/24
  - Fingerprint อุปกรณ์สแกนลายนิ้วมือ