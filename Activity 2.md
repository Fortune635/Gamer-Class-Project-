"""
🎭 Polymorphism Challenge – Activity 2
Author: Fortune Akioya
Date: October 2025

Description:
This program demonstrates the concept of polymorphism in Object-Oriented Programming (OOP).
It includes multiple classes (Car, Plane, Boat) that define the same method `move()` differently.

Each class represents a different type of vehicle, but they all share a common interface — the `move()` method.
This allows the same function to behave differently depending on the object that calls it.
"""

# ------------------ Code Starts Here ------------------

# Base class
class Vehicle:
    def move(self):
        print("The vehicle is moving...")

# Subclasses demonstrating polymorphism
class Car(Vehicle):
    def move(self):
        print("🚗 The car is driving on the road.")

class Plane(Vehicle):
    def move(self):
        print("✈️ The plane is flying in the sky.")

class Boat(Vehicle):
    def move(self):
        print("⛵ The boat is sailing on the water.")

# Function demonstrating polymorphism
def vehicle_movement(vehicle):
    vehicle.move()

# Create objects of each class
car = Car()
plane = Plane()
boat = Boat()

# Call the same method on different objects
vehicle_movement(car)
vehicle_movement(plane)
vehicle_movement(boat)
