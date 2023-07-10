---
title: "Medical System"
permalink: /docs/medical-equipment-system/
excerpt: "การเชื่อมอุปกรณ์การแพทย์"
last_modified_at: 2023-07-10T17:48:05-04:00
redirect_from:
  - /theme-setup/
toc: true
---

## ข้อมูลทั่วไป

<div align="center">
  <pre class="mermaid">
    mindmap
    root((Vender<br/>broker))
        Based site monitor
        ::icon(fa fa-heartbeat)
        12 lead ecg
        ::icon(fa fa-heartbeat)
  </pre>
</div>

- Vender broket อุปกรณ์ที่พัฒนาโดย บริษัทภายนอก เพื่อแปลงข้อมูลจากอุปกรณ์การแพทย์ ให้เป็นรูปแบบมาตฐาน HL7 เพื่อให้ ETO Gateway ส่งข้อมูลไปยังระบบอื่นต่อไป
- Based site monitor
- 12 lead ecg

## ระบบ api
// TODO
<!-- <div>
<iframe src="/eto-doc/openapi-1.html" title="ETO api"></iframe>
</div> -->

<div>
  <!DOCTYPE html>
  <html lang="en">

  <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1">
      <link rel="stylesheet" type="text/css"
          href="https://cdnjs.cloudflare.com/ajax/libs/swagger-ui/5.1.0/swagger-ui.min.css">
      <title>ETO api</title>

  <body>
      <div id="openapi">
          <script src="https://cdnjs.cloudflare.com/ajax/libs/swagger-ui/5.1.0/swagger-ui-bundle.min.js"></script>
          <script>
              window.onload = function () {
                  const ui = SwaggerUIBundle({
                      url: "/eto-doc/assets/openapi/vitual-1.json",
                      dom_id: "#openapi"
                  })
              }
          </script>
  </body>
</div>
