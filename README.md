#drawing
import turtle

def draw_shiva_complete():
    s = turtle.Screen()
    s.bgcolor("#1a1a1a")  # Dark background
    t = turtle.Turtle()
    t.speed(0) # Fastest speed

    # 1. Face Outline & Neck
    t.penup()
    t.goto(0, -150)
    t.pendown()
    t.color("#f2d1b3") # Skin tone
    t.begin_fill()
    t.circle(150) 
    t.end_fill()
    
    # Blue Neck (Neelkanth)
    t.penup()
    t.goto(-60, -150)
    t.pendown()
    t.color("#4a90e2")
    t.begin_fill()
    t.setheading(-90)
    t.forward(50)
    t.setheading(0)
    t.forward(120)
    t.setheading(90)
    t.forward(50)
    t.end_fill()

    # 2. Matted Hair (Jata)
    t.penup()
    t.goto(-150, 100)
    t.color("#3e2723")
    t.setheading(90)
    t.pendown()
    t.begin_fill()
    for _ in range(2):
        t.circle(-50, 180)
        t.circle(50, 180)
    t.goto(150, 100)
    t.goto(0, 250)
    t.goto(-150, 100)
    t.end_fill()

    # 3. Tripundra (Tilak)
    t.penup()
    t.goto(-70, 60)
    t.setheading(0)
    t.color("white")
    t.pensize(5)
    for i in range(3):
        t.pendown()
        t.forward(140)
        t.penup()
        t.goto(-70, 60 - (i+1)*15)

    # 4. The Third Eye (Red)
    t.penup()
    t.goto(0, 10)
    t.color("red")
    t.pendown()
    t.begin_fill()
    t.setheading(45)
    for _ in range(2):
        t.circle(25, 90)
        t.circle(25//2, 90)
    t.end_fill()

    # 5. Eyes (Closed in Meditation)
    t.pensize(3)
    t.color("black")
    # Left Eye
    t.penup()
    t.goto(-80, -10)
    t.setheading(-30)
    t.pendown()
    t.circle(40, 60)
    # Right Eye
    t.penup()
    t.goto(40, -10)
    t.setheading(-30)
    t.pendown()
    t.circle(40, 60)

    # 6. The Snake (Vasuki)
    t.penup()
    t.goto(70, -160)
    t.color("#4caf50")
    t.pensize(8)
    t.setheading(45)
    t.pendown()
    t.circle(50, 220)
    # Snake Head
    t.begin_fill()
    t.circle(10)
    t.end_fill()

    # 7. Crescent Moon
    t.penup()
    t.goto(80, 180)
    t.color("silver")
    t.setheading(30)
    t.pendown()
    t.begin_fill()
    t.circle(40, 160)
    t.setheading(190)
    t.circle(-35, 150)
    t.end_fill()

    t.hideturtle()
    print("Har Har Mahadev!")
    s.exitonclick()

if __name__ == "__main__":
    draw_shiva_complete()
