# C++ Class
* [โครงสร้าง Class](#S-class-structure)
## <a name="S-class-structure"></a>โครงสร้าง Class
```
class ชื่อคลาส {
    access specifier : สมาชิกของคลาส
};
```
|ตัวระบุการเข้าถึง (Access specifiers)|คำอธิบาย|
|:---|:--|
|`public`|สมาชิกของคลาสสามารถเข้าถึงได้จากนอก class ทั้งจาก subclass และจาก main()|
|`private`|สมาชิกของคลาสเข้าถึงได้เฉพาะภายใน class|
|`protected`|สมาชิกของคลาสสามารถเข้าถึงได้จาก subclass แต่ไม่สามารถเข้าถึงได้จาก main()|

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
```
class Student {
    public:
        void setName(std::string&); // forward declaration
    private:
        std::string name;
};
// member function definition
void Student::setName(std::string& n) {
    name = n;
}
int main() {
    Student student1;           // สร้าง Object ชื่อ student1
    student1.setName("Alice");  // ok, setName เป็น publice
    student1.name = "Alice";    // error เพราะ name เป็น private
    return 0;
}
```
