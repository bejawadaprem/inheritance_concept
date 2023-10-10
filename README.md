# inheritance_concept
# Parent class (base class)
class Vehicle:
    def __init__(self, company, model, year):
        self.company = company
        self.model = model
        self.year = year

    def display_info(self):
        print("Company:",self.company)
        print("Model:",self.model)
        print("Year:",self.year)

# Child class (subclass) inheriting from Vehicle
class Car(Vehicle):
    def __init__(self, company, model, year, capacity):
        # Call the constructor of the parent class using super()
        super().__init__(company, model, year)
        self.capacity = capacity

    def display_info(self):
        # Call the overridden method of the parent class
        super().display_info()
        print("Seating Capacity :" ,self.capacity)

# Child class (subclass) inheriting from Vehicle
class Motorcycle(Vehicle):
    def __init__(self, company, model, year, engine_type):
        # Call the constructor of the parent class using super()
        super().__init__(company, model, year)
        self.engine_type = engine_type

    def display_info(self):
        # Call the overridden method of the parent class
        super().display_info()
        print("Engine Type:",self.engine_type)

# Creating instances of the child classes
car = Car("TATA", "NIXON", 2023, 4)
motorcycle = Motorcycle("RE-HIMAYALAN", "CBR500R", 2023, "Inline-4")

# Displaying information about the vehicle objects
print("Car Information:")
car.display_info()
print("\nMotorcycle Information:")
motorcycle.display_info()
