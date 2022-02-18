# Union และ Struct
```
struct X { int a = 1, b = 2; };

union U
{
    X x;
    struct Y { int c = 3, d = 4, e = 5; };
    struct Z;   // forward declaration
};

struct U::Z {
    int n;
    int m;
};
```
