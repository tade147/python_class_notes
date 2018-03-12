# python_class_notes
learning notes about python_class

1.创建和使用类
1.1创建dog类
class Dog():
    """一次模拟小狗的简单尝试"""


    def _init_(self, name, age):
        """初始化属性name和age"""
        self.name = name
        self.age = age


    def sit(self):
        """模拟小狗被命令时蹲下"""
        print(self.name.title() + " is now sitting.")

    def roll_over(self):
        """模拟小狗被命令时打滚"""
        print(self.name.title() + " rolled over!")

注意：类的首字母用大写；_init_（）。
        
2 使用类和实例
2.1 Car类
class Car():
    """一次模拟汽车的简单尝试"""
    def __init__(self, make, model, year):
        """初始化描述汽车的属性"""
        self.make = make
        self.model = model
        self.year = year

    def get_descriptive_name(self):
        """返回整洁的描述信息"""
        long_name = str(self.year) + ' ' +self.make + ' ' + self.model
        return long_name.title()

my_new_car = Car('audi', 'a4', 2016)
print(my_new_car.get_descriptive_name())


2.2 给属性制定默认值
class Car():
    """一次模拟汽车的简单尝试"""
    def __init__(self, make, model, year):
        """初始化描述汽车的属性"""
        self.make = make
        self.model = model
        self.year = year
        self.odometer_reading = 0

    def get_descriptive_name(self):
        """返回整洁的描述信息"""
        long_name = str(self.year) + ' ' +self.make + ' ' + self.model
        return long_name.title()

    def read_odometer(self):
        """打印一条指出汽车历程的消息"""
        print("This car has " + str(self.odometer_reading) + " miles on it.")

my_new_car = Car('audi', 'a4', 2016)
print(my_new_car.get_descriptive_name())
my_new_car.read_odometer()

2.3  修改属性的值
（1）直接修改属性的值
class Car():
    """一次模拟汽车的简单尝试"""
    def __init__(self, make, model, year):
        """初始化描述汽车的属性"""
        self.make = make
        self.model = model
        self.year = year

    def get_descriptive_name(self):
        """返回整洁的描述信息"""
        long_name = str(self.year) + ' ' +self.make + ' ' + self.model
        return long_name.title()

    def read_odometer(self):
        """打印一条指出汽车历程的消息"""
        print("This car has " + str(self.odometer_reading) + " miles on it.")

my_new_car = Car('audi', 'a4', 2016)
print(my_new_car.get_descriptive_name())
my_new_car.odometer_reading = 23
my_new_car.read_odometer()

（2）通过方法修改属性的值
class Car():
    """一次模拟汽车的简单尝试"""
    def __init__(self, make, model, year):
        """初始化描述汽车的属性"""
        self.make = make
        self.model = model
        self.year = year

    def get_descriptive_name(self):
        """返回整洁的描述信息"""
        long_name = str(self.year) + ' ' +self.make + ' ' + self.model
        return long_name.title()

    def read_odometer(self):
        """打印一条指出汽车历程的消息"""
        print("This car has " + str(self.odometer_reading) + " miles on it.")

    def update_odometer(self, mileage):
        """将里程表读数设置为指定的值"""
        self.odometer_reading = mileage

my_new_car = Car('audi', 'a4', 2016)
print(my_new_car.get_descriptive_name())
my_new_car.update_odometer(23)
my_new_car.read_odometer()

（3）通过方法对属性的值进行递增
class Car():
    """一次模拟汽车的简单尝试"""
    def __init__(self, make, model, year):
        """初始化描述汽车的属性"""
        self.make = make
        self.model = model
        self.year = year

    def get_descriptive_name(self):
        """返回整洁的描述信息"""
        long_name = str(self.year) + ' ' +self.make + ' ' + self.model
        return long_name.title()

    def read_odometer(self):
        """打印一条指出汽车历程的消息"""
        print("This car has " + str(self.odometer_reading) + " miles on it.")

    def update_odometer(self, mileage):
        """将里程表读数设置为指定的值"""
        self.odometer_reading = mileage

    def increment_odometer(self, miles):
        """将里程表读数增加指定的量"""
        self.odometer_reading +=miles

my_used_car = Car('audi', 'a4', 2016)
print(my_used_car.get_descriptive_name())

my_used_car.update_odometer(23500)
my_used_car.read_odometer()

my_used_car.increment_odometer(100)
my_used_car.read_odometer()

3.继承
3.1 子类的方法 __init__()


