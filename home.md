---
layout: splash
permalink: /
hidden: true
header:
  overlay_color: "#5e616c"
  actions:
    - label: "<i class='fa fa-file-text-o'></i> ภาพรวมระบบ"
      url: "/docs/quick-guide/"
excerpt: >
  ETO เป็นสื่อกลางในการเชื่อมโยงระบบข้อมูลการแพทย์บนพาหนะ ทางบก หรือ ทางอาศ เพื่อให้บริการอื่นเชื่อมต่อผ่านระบบ api ที่ใช้มาตฐานเดียวกัน
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

        Software
            Network monitor
            Gateway monitor
            Vital sign api

        Panel Pc/Tablet
        ::icon(fa fa-tablet)
            Mic
            ::icon(fa fa-microphone)
            Speaker
            ::icon(fa fa-volume-up)
            Software
                D1669 Medinfo

        Wifi Hotspot
        ::icon(fa fa-wifi)
  </pre>
</div>