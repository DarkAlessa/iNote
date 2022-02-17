# C++ Class
* [การประกาศคลาส (Class declaration)](#S-class-structure)   
## <a name="S-class-structure"></a>การประกาศคลาส (Class declaration)
```
class-key class-name {member-specification};
```
* class-key :   เช่น class, struct, union   
* class-name : ชื่อคลาส   
* [member-specification](#S-member-specification) : รายการของ access-specifiers, data member และ member function   

## การประกาศล่วงหน้า (Forward declaration)
```
class-key identifier;
```
เป็นการประกาศคลาสแต่ไม่มีการนิยามคลาส (definition)
```
class Student;      // forward declaration
class Student {     // class definition
    ...
};
```
## <a name="S-member-specification"></a>Member Specification
### Access specifiers
`public`    สมาชิกของคลาสสามารถเข้าถึงได้จากนอก class ทั้งจาก subclass และจาก main()   
`private`   สมาชิกของคลาสเข้าถึงได้เฉพาะภายใน class   
`protected` สมาชิกของคลาสสามารถเข้าถึงได้จาก subclass แต่ไม่สามารถเข้าถึงได้จาก main()   
>\*สมาชิกของคลาสหมายถึง `Data Members` และ `Member Functions`   
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
