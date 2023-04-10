# Design notebook entry

## Last week's critique

Last week I got feedback on my implementation of an "arc" type syntax, and 
whether or not to do an internal or external language. I really appreciated
the input from my group and Prof Ben, and it was helpful to get other eyes on what I was stuck on, 
especially for figuring out arc. I think I have a better syntax idea now than I did a week
ago, which I feel more comfortable and excited about. For deciding on internal vs external,
I did end up going with my original idea of an external language. Learning to use python
parser combinators is proving to be enough of a challenge that I don't feel like I 
chose just the easy route. 

## Description

This week I had two main goals for myself - to start the implementation process by
creating a parser and having a working super basic program, and to figure out what
the arc syntax was going to be. I made a lot of progress, though didn't quite get
to where I hoped (as of 9pm Sunday night).

For arc, I decided to keep the actual drawing as straight lines, and then add a
parameter for the user to specify how "curved" something is, and then the implementation
figures out how to make it a bezier curve. I think this will be more intuitive than
trying to write an arc, though it might limit some of what the program can do.
Ultimately, I decided fluency was more important, and this still allows the user a
great deal of flexibility in the shape of the design. So, we can instead create 
something like this

![Complicated Panto](images/morecomplex_panto.PNG)

propogate: vertical

design:

curve 5

draw 50

turn right 90

draw 15

turn right 90

draw 10

turn right 90

draw 10

turn right 90

draw 20

turn right 90

draw 20

turn right 90

draw 20

turn right 90

draw 20

turn right 90

draw 20

turn left 90

draw 15

turn left 90

draw 10

turn left 90

draw 10

turn left 90

draw 20

turn left 90

draw 20

turn left 90

draw 20

turn left 90

draw 20

turn left 90

draw 20

For the implementation work, I decided to use Antlr, which is very
cool but also very complex. There has been a larger learning curve than
expected, because I had to determine which of the generated parse tree,
listener, etc I should use and what I needed to override. As of right now,
I have a parser that generates a parse tree correctly, and am working
on debugging the visitor that essentially creates an interpreter for
the parse tree. I am confident that I understand the concept of what I'm 
supposed to do, it's just the how of it has taken more time than expected.
But I think after I get the visitor to instantiate correctly, I'll be able
to parse more complicated things easier.

## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

Right now there is the practical side of the project, which is debugging
the visitor that is pretty pressing - I want it to be able to do something!
I do also want to spend some time this week thinking about errors and what
possible errors might occur, both parsing and semantics, to start working
on communicating those errors as I go rather than back-tracking. 

**What questions do you have for your critique partners? How can they best help
you?**

I have a question about fluency for the scale of the drawings - what would make
the most sense when I think about "moving forward." Right now it is written like
"steps" that the turtle is taking, in the direction that it is facing. Does it make
more sense to let the scale be in the control of the user, or automatically scale it
based on what I know the screen size to be so that they don't have to? Because I'm 
thinking smaller numbers, like 2 - 20 can be thought of like inches, rather than the 
500 x 500 screen size of pixels. 

**How much time did you spend on the project this week? If you're working in a
team, how did you share the work?**
Around 9-10 hours.

**Compared to what you wrote in your contract about what you want to get out of this
project, how did this week go?**
I think it went ok! I know that I didn't get as much done as I wanted, but I also put
in the time and effort and learned alot already so I feel proud of what I did manage
to do.
