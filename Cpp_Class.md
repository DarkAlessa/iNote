# C++ Class
โครงสร้าง class
```
class class-name {
    public : member-declaration
    private : member-declaration
    protected : member-declaration
};
```
|ตัวระบุการเข้าถึง (Access specifiers)|คำอธิบาย|
|:---|:--|
|`public`|สมาชิกของ class สามารถเข้าถึงได้จากนอก class ทั้งจาก subclass และจาก main()|
|`private`|สมาชิกของ class เข้าถึงได้เฉพาะภายใน class|
|`protected`|สมาชิกของ class สามารถเข้าถึงได้จาก subclass แต่ไม่สามารถเข้าถึงได้จาก main()|

>สมาชิกของ class หมายถึง `Data Members` และ `Member Functions`<br>
>ถ้าไม่ระบุ access specifier สมาชิกของคลาสจะเป็น private

ตัวอย่าง
```
class Student {
    public:
        // member function ชื่อ setName
        void setName(std::string n) {
            name = n;
        }
    private:
        std::string name; // data member ชื่อ name
};
```
