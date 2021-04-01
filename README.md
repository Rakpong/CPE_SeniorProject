# CPE_SeniorProject
AutomaticFireDetectionSystem ระบบตรวจจับไฟไหม้
จัดทำโดย นายรักษ์พงศ์ทอหุล มีวัตถุประสงค์เพื่อ
> - ช่วยในการตรวจจับไฟไหม้ป่าจากหอดูไฟที่เดิมแล้วใช้เจ้าหน้าที่ในการตรวจจับโดยในโปรเจคนี้ได้ทำการพัฒนาโมเดลที่ใช้ในการทำนายควันไฟจากไฟไหม้ จากรูปภาพ โดยทำออกมาในลักษณะเว็บแอพพลิเคชั่นที่รับอินพุตเป็นไฟล์วิดีโอเพื่อจำลองการทำงานบนหอดูไฟนั่นเอง

## OVERVIEW SYSTEM 
แบ่งเป็นสามส่วนหลัก ๆ คือ
1. Machine Learning ส่วนโมเดลที่พัฒนาโดยใช้ Convolutional Neural Network ใช้ในการทำนายภาพว่ามีควันไฟหรือไม่
2. Flask API ที่นำโมเดลที่เทรนแล้วมาใช้ในระบบ
3. ส่วน Web-app ที่ใช้แสดงผลโดยใช้ react

## INSTALLATION
แบ่งเป็นสองส่วนคือ API และ Web-app เนื่องจากส่วนของโมเดลได้มีการเทรนด้วยข้อมูลมาแล้วและได้ทำการ save model ไว้ในส่วน API แล้วหากต้องการดูในส่วนโมเดลสามารถดูตาม source code -> Model ได้เลย

### Flask API
ทำการ create venv แล้ว activate venv จากนั้นทำการติดตั้ง flask ตาม document นี้
> - [flask install](https://flask.palletsprojects.com/en/1.1.x/installation) 
จากนั้นทำการติดตั้ง library ที่จำเป็นใน venv ดังนี้
```python
pip install tensorflow
pip install numpy
pip install matplotlib
pip install opencv-python
```
npm install base-64

### Web-application
ทำการสร้าง mode module ตาม document ดังนี้
> - [react setup](https://reactjs.org/docs/create-a-new-react-app.html) 
จากนั้นทำการติดตั้ง library ที่จำเป็นดังนี้
> - npm install react-player # or yarn add react-player