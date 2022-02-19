# C++ Class
* [การประกาศคลาส (Class declaration)](#S-class-structure)   
## <a name="S-class-structure"></a>การประกาศคลาส (Class declaration)
```
class-key class-name {
    member-specification
};
```
* class-key :   เช่น class, struct, union   
* class-name : ชื่อคลาส   
* [member-specification](#S-member-specification) : รายการของ access-specifiers, data member และ member function   

## การประกาศล่วงหน้า (Forward declaration)
เป็นการประกาศคลาสโดยที่ยังไม่มีการนิยามคลาส(definition) ในขณะที่ประกาศ โดยจะนิยามคลาสภายหลัง
```
class-key class-name;
```
ตัวอย่างการประกาศล่วงหน้าและการนิยามคลาส
```
class Student;      // forward declaration
class Student {     // class definition
    ...
};
```
\*[object](https://en.wikipedia.org/wiki/Object_(computer_science)) และ non-inline function ไม่สามารถมีนิยามมากกว่าหนึ่งนิยามตามกฎของ [One Definition Rule](https://en.wikipedia.org/wiki/One_Definition_Rule)   
## <a name="S-member-specification"></a>Member Specification
### ตัวระบุการเข้าถึง (Access specifiers)
`public`    สมาชิกของคลาสสามารถเข้าถึงได้จากนอก class ทั้งจาก subclass และจาก main()   
`private`   สมาชิกของคลาสเข้าถึงได้เฉพาะภายใน class   
`protected` สมาชิกของคลาสสามารถเข้าถึงได้จาก subclass แต่ไม่สามารถเข้าถึงได้จาก main()   
>\*สมาชิกของคลาสหมายถึง `Data Members` และ `Member Functions`   
>\*ถ้าไม่ระบุ access specifier สมาชิกของคลาสจะเป็น private   

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
### Constructors
![Constructors](https://media.geeksforgeeks.org/wp-content/cdn-uploads/20191128195435/CPP-Constructors.png)
