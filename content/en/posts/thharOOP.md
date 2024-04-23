---
title: "Thhar, and a rant about OOP"
date: 2024-04-17

---
## Why
In 2023 I and a couple of friends have joined [Motorola science cup](https://science-cup.pl/) competition. One of our tasks was to design and code up a clone of an arcade classic [Battlezone](https://en.wikipedia.org/wiki/Battlezone_(1980_video_game)). And while i won't publish the whole game under my name since it was a collaborative effort. The engine was written by myself with a help of a few articles and similar projects see the *Sources* section.

## Ebiten and Go
This is my first [Go](https://go.dev/) experience, coming from [Python](https://www.python.org/) I immediately fell in love with the staticly typed nature of the language. 

In any large [Python](https://www.python.org/) project I was already using *type hints*, since if you don't use them you are guaranteed to be miserable, so the switch wasn't hard. And with new features like the new loop syntax(new to [Go](https://go.dev/) ofc.), allowing you to iterate through numbers
```go
    for i := range(10){
        // Important Stuff
    }
```
the language seemed really approachable

### Free from OOP
Don't get me wrong I still enjoy OO coding. I was just finding that as my requirement for more and more advanced libraries grew so did the number of useless classes and children. It got to the point of almost being [Java](https://www.java.com/en/), my UI was a class, my database connection was made with an ORM, my network responses were classes. Changing one variable name was always stressful, wait have i used it somewhere else, will the refactor functionality work?...

When using python I have used PyQT6 to develop my Apps. It seemed like the easiest solution, with an easy drag to place designer. Of course the design was then translated to a class. Why??? Then I fell in love with the web as an interface for my applications. Everything is nicely structured, layout is separated from styling and the logic can be on the other side of the earth. It allows me to easily separate tasks, when I do logic I do logic, when it is time for some creative work with *css* i do creative logic. Nothing overlaps and that's how it should be 

## The Engine 
The code in itself is not the most important part of the story. It uses [ebiten](https://ebitengine.org/) as a 2d graphics library. The pipeline is simple, since for now it only allows for rendering of wireframe-s:

1. Load the object model from an [Wavefront `.obj` File](https://en.wikipedia.org/wiki/Wavefront_.obj_file) 
2. Calculate the position of the camera
3. Calculate the positions of vertexes, and join them together according to the specified faces.
4. Display to the user.

## Example usage, Demos
For the demo check out my [Demos](/en/demos) page.

## Sources
This engine was originally based on a similar [Python](https://www.python.org/) project by [StanislavPetrovV](https://github.com/StanislavPetrovV/Software_3D_engine) and another project created by [tvytlx](https://github.com/tvytlx/render-py)
