# Ali-Muttaleb
# This is going to be a random walk
from turtle import *
from random import randint
from colorsys import hsv_to_rgb

step = 30 #length of each step
nsteps=2000
hinc=1.0/nsteps
width(2)  #width of the line

(w, h)=screebsize() #setting the boundari of walk
speed('fastest')
colormode(1,0)
bgcolor('black')
hue=0.0
for i in range(nstps):
    setheading(randint(0,359))
    color(hsv_to_rgb(hue, 1.0, 1.0)) #pen color in RGB
    hue+=hinc #change color
    forward(step)
    (x, y)=pos()
    if abs(x)>w or abs(y)>h:
        backward(step)
        turtle.done()
