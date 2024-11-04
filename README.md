we can define a structure called Shape that includes both a Square and a Rectangle as its members. The Square structure will have an area attribute, while the Rectangle structure will have length and breadth attributes.

Steps:
1.Define a structure Square with an integer area attribute.
2.Define a structure Rectangle with integer length and breadth attributes.
3.Define a Shape structure that contains Square and Rectangle as its members.
4.Demonstrate usage by creating a Shape object, setting values for square area, rectangle length, and breadth, and calculating/displaying the rectangle area as well.

Code Implementation:

#include <stdio.h>

// Define the Square structure with area as an attribute
struct Square {
    int area;
};

// Define the Rectangle structure with length and breadth as attributes
struct Rectangle {
    int length;
    int breadth;
};

// Define the Shape structure that encompasses both Square and Rectangle
struct Shape {
    struct Square square;
    struct Rectangle rectangle;
};

int main() {
    
    // Declare a Shape object
   
    struct Shape shape;

    // Initialize Square's area
    int side = 4;  // Example side length for the square
    shape.square.area = side * side;  // Calculate area for a square of given side

    // Initialize Rectangle's length and breadth
    shape.rectangle.length = 5;  // Example length for the rectangle
    shape.rectangle.breadth = 3;  // Example breadth for the rectangle

    // Calculate Rectangle's area
    int rectangleArea = shape.rectangle.length * shape.rectangle.breadth;

    // Display the results
    printf("Square:\n");
    printf(" - Side: %d\n", side);
    printf(" - Area: %d\n\n", shape.square.area);

    printf("Rectangle:\n");
    printf(" - Length: %d\n", shape.rectangle.length);
    printf(" - Breadth: %d\n", shape.rectangle.breadth);
    printf(" - Area: %d\n", rectangleArea);

    return 0;
}

Explanation
1.Structure Definitions:

a.Square: Contains an area attribute for storing the area of the square.
b.Rectangle: Contains length and breadth attributes for the dimensions of the rectangle.
c.Shape: Contains both Square and Rectangle as data members.

2.Main Function:

a.We declare an object shape of type Shape.
b.We assign values to the square's side and calculate its area, storing it in shape.square.area.
c.We assign values to the rectangle's length and breadth, then calculate the rectangle's area.
d.Finally, we print the side and area of the square, as well as the length, breadth, and area of the rectangle.

