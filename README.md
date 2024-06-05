#Завдання 1
class Car:
    def __init__(self, make, model, year):
        self.make = make
        self.model = model
        self.year = year
        self.speed = 0
    def accelerate(self):
        self.speed += 5
    def brake(self):
        self.speed -= 5
    def get_speed(self):
        return self.speed
car = Car("Toyota", "Camry", 2020)
for _ in range(5):
    car.accelerate()
    print("Current speed:", car.get_speed())
for _ in range(5):
    car.brake()
    print("Current speed:", car.get_speed())

    #Завдання 2
    
class Buffer:
    def __init__(self):
        self.buffer = []
    def add(self, *a):
        self.buffer.extend(a)
        while len(self.buffer) >= 5:
            print(sum(self.buffer[:5]))
            self.buffer = self.buffer[5:]
    def get_current_part(self):
        return self.buffer
buffer = Buffer()
buffer.add(1, 2, 3, 4, 5)
buffer.add(6, 7, 8, 9, 10)
buffer.add(11, 12, 13, 14, 15)

print("Current part of the buffer:", buffer.get_current_part())

