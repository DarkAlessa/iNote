# C++ Class
* [การประกาศคลาส (Class declaration)](#S-class-structure)
## <a name="S-class-structure"></a>การประกาศคลาส (Class declaration)
```
class class-name {
    access-specifier : member-specification
};
```
Access Specifier
|ตัวระบุการเข้าถึง (Access specifiers)|คำอธิบาย|
|:---|:--|
|`public`|สมาชิกของคลาสสามารถเข้าถึงได้จากนอก class ทั้งจาก subclass และจาก main()|
|`private`|สมาชิกของคลาสเข้าถึงได้เฉพาะภายใน class|
|`protected`|สมาชิกของคลาสสามารถเข้าถึงได้จาก subclass แต่ไม่สามารถเข้าถึงได้จาก main()|
Member Specification
|member-specification|คำอธิบาย|
|:---|:--|


>\*สมาชิกของคลาสหมายถึง `Data Members` และ `Member Functions`<br>
>\*ถ้าไม่ระบุ access specifier สมาชิกของคลาสจะเป็น private

ตัวอย่าง
```
class Student {
    public:
        // member function ชื่อ setName
        void setName(std::string& n) {
            name = n;
        }
    private:
        std::string name; // data member ชื่อ name
};
```
