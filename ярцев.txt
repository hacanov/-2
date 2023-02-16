class A:
    def __init__(self, prop1, prop2):
        self.prop1 = prop1
        self.prop2 = prop2

    def method1(self):
        print("Method 1 of class A")

    def method2(self):
        print("Method 2 of class A")

    def method3(self):
        print("Method 3 of class A")


class B(A):
    def __init__(self, prop1, prop2, prop3):
        super().__init__(prop1, prop2)
        self.prop3 = prop3

    def method3(self):
        print("Method 3 of class B")


class C(A):
    def __init__(self, prop1="default_prop1", prop2="default_prop2"):
        super().__init__(prop1, prop2)

    def method4(self):
        print("Method 4 of class C")

    def method5(self):
        print("Method 5 of class C")


a = A("prop1_value", "prop2_value")
b = B("prop1_value", "prop2_value", "prop3_value")
c = C()

a.method1()
a.method2()
a.method3()

b.method1()
b.method2()
b.method3()

c.method1()
c.method2()
c.method3()
c.method4()
c.method5()