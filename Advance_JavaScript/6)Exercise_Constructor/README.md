# Homework_codecamp_8
### Advance JavaScript Exercise Constructor กับ New
ธนกฤต ชัยวานิชกุล

Exercise Constructor กับ New
1.สร้าง constructor function ที่ใช้สำหรับสร้าง Calculator โดยต้องมี 3 Methods นี้
- read(): รับค่าจาก propmt สองตัว
- sum(): ให้คืนค่าจากการบวกกันของตัวแปรสองตัว
- mul(): ให้คืนค่าจากการคูณกันของตัวแปรสองตัว
```
function Calculator() {
  this.read = function() {
    this.x = Number(prompt('please input the 1st value'))
    this.y = Number(prompt('please input the 2nd value'))
  },
  this.sum = function() {
    return this.x + this.y
  },
  this.mul = function() {
    return this.x * this.y
  }
}

```
2.สร้าง constructor function Accumulator(startingValue)
- โดยที่ Object ดังกล่าวควร เก็บผลรวมไว้ใน property ที่มี key ชื่อว่า value, ค่าเริ่มต้นของ key ชื่อ value นี้ คือ startingValue
- ฟังก์ชัน read() ควรอ่านค่าจาก propmt() และ เพิ่มค่าที่ใส่เข้ามาใน key ชื่อ value
พูดง่าย ๆ ก็คือ value คือผลรวมของ prompt โดยเริ่มจาก startingValue
```
function Accumulator(startingValue) {
  this.value = startingValue,
  this.read = function() {
    this.value += Number(prompt('please add a number to value'))
  }
}

```
