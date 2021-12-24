---
layout: post
title: Flex in css
subtitle: CSS Flexbox คืออะไร + สอนวิธีใช้
tags: [flex, css]
---

ใน CSS 2.1 เราจะใช้สิ่งที่เรียกว่า “Layout Mode” ในการกำหนดขนาด และจัดตำแหน่งของกล่องต่างๆ ซึ่ง layout mode นี้จะประกอบไปด้วย<br/>
<br/>
  - blockใช้จัดตำแหน่งเนื้อหาให้อยู่ในรูปแบบของ block
  - inlineใช้จัดตำแหน่งเนื้อหาให้อยู่ในรูปแบบของ text
  - tableใช้จัดตำแหน่งเนื้อหาให้อยู่ในรูปแบบตาราง
  - positionใช้จัดตำแหน่งของ elements ต่างๆ ได้อย่างอิสระมากขึ้น
  
  ด้วยความซับซ้อนที่มากขึ้นของ web สมัยใหม่ การใช้ layout mode แบบเดิมๆ อาจทำให้เราเขียนโค้ดได้ไม่ค่อยสะดวกนัก CSS 3 จึงได้เพิ่ม layout mode แบบใหม่ ที่เรียกว่า “Flex Layout” เข้ามา โดย flex layout นี้เอง ที่จะช่วยให้กล่องต่างๆ มีความยืดหยุ่นมากขึ้น (Flexible Box หรือเรียกสั้นๆ ว่า Flexbox)
flex layout จะมีความคล้ายคลึงกับ block layout เพียงแต่ว่ามันจะใช้ property บางอย่าง เช่น float ไม่ได้ ในทางกลับกัน มันจะมี property ใหม่ๆ เพิ่มเข้ามาให้เราใช้งาน โดยความสามารถหลักๆ ของ flex layout มีดังนี้

  - Orientationสามารถกำหนดแนวการเรียงของ flexbox ต่างๆ ได้ ไม่ว่าจะเป็น บนลงล่าง ล่างขึ้นบน ซ้ายไปขวา ขวาไปซ้าย
  - Sizingสามารถกำหนดขนาดของ flexbox ต่างๆ ให้พอดีกับพื้นที่ว่างที่เหลืออยู่ได้อย่างอัตโนมัติ
  - Orderingสามารถเลือกลำดับการแสดงผลของ flexbox ได้ ลำดับของ flexbox อาจแตกต่างกันไปในแต่ละขนาดของ viewport
  - Alignmentสามารถกำหนด alignment ของ flexbox ต่างๆ ได้ ไม่ว่าจะเป็น ชิดซ้าย กึ่งกลาง หรือชิดขวา ทั้งในแนวนอนและแนวตั้ง
  
  จะใช้ Flexbox ต้องทำอย่างไร ?
มาดูคำศัพท์เกี่ยวกับ flexbox ที่ต้องรู้กันก่อน
  - Flex containerคือ html element ที่กำหนด property “display” ให้มีค่าเป็น “flex” หรือ “inline-flex”
  - Flex itemหมายถึง html elements ใดๆ ก็ตาม ที่เป็น child ของ flex container
  
  ก่อนที่เราจะสามารถใช้ความสามารถต่างๆ flexbox ได้ เราจะต้องสร้าง “flex container” ขึ้นมาก่อน โดยปกติแล้ว เวลาเราจะใช้ layout mode กับ elements ไหน เราก็จะต้องใส่ property “display” เอาไว้ที่ elements นั้นๆ แต่การใช้ flexbox จะเปลี่ยนไปตรงที่ เราจะต้องกำหนด property “display” เอาไว้ที่ element ที่เป็น container แทน ลองดูตัวอย่างโค้ดต่อไปนี้
  
  ```
    <div class="flex-container">
      <div>flex item 1</div>
      <div>flex item 2</div>
      <div>flex item 3</div>
    </div>
    
    .flex-container{
    display: flex;
    }
```
