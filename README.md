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
        
