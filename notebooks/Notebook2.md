# Design notebook entry

## Last week's critique

**TODO:** Fill in this part with a summary and reflection on the critique you received for
last week's work. Answer questions such as:  How, specifically, did the feedback help
improve the project? Did the feedback point out or offer something you hadn't considered?
Did it help you make a design decision? Was it helpful in addressing the most pressing
issues in your project? How will you incorporate the feedback into your work? Will you
change something about the design, implementation, or evaluation as a result?

In class last week, I asked two specific questions for feedback and I recieved
feedback on this both in class an through the github feedback. The first question
I asked was if I should implement the parser or compiler first, and the second
question I asked was for them to look at my example programs to see what they
thought of them. We had a group discussion about writing the parser or compiler
first, and agreed together that it would probably be easier to write our parsers
first. Kate noted in the feedback too that it is great to start with a simple
parser and then add is more later as I work on the compiler. Now that I have
done this, I am very happy that I wrote the parser first and will be working
on the compiler next.

When showing them my example programs, there were no negative critiques. I asked
specifically about the splitting up of content into different files, which Kate
said she really liked. We discussed the idea that maybe the language could
allow the user to either write in the same file or write in multiple files, as
my import statement would be basically copying and pasting the content of a
different file into the current one. I really really like this idea, as you
get the benefits of having multiple files, but still allow users the choice.

Kate also noted that it is great that everybody in our group is using python as
a host language. This way we can all help each other!

All of this feedback was helpful to me in confirming the success of what I have
worked on so far, and preparing me to start learning about writing my parser. 

## Description

**TODO:** Fill in this part with information about your work this week:
important design decisions, changes to previous decisions, open questions,
exciting milestones, preliminary results, etc. Feel free to include images
(e.g., a sketch of the design or a screenshot of a running program), links to
code, and any other resources that you think will help clearly convey your
design process.

This week began with our feedback session on Monday, I also gave Ryder feedback
on his work after class on Monday.

Afterwards, I worked on the project significantly Tuesday afternoon until I 
reached a point where I was stuck with questions, got my questions answered in
class on Wednesday, and then continued ahead until I was done with my basic parser
on thursday afternoon.

On Tuesday afternoon I started by drafting my abstract syntax tree (AST) based on
my example programs. I then followed the advice from the class grutor to look
into python parsers. I first tried ANTLR, but I was having trouble getting it to
work properly so I moved on to working with funcparserlib. The grutor suggested
using funcparserlib because it has great documentation, which I agree with! There
is a built in step by step intro guide which I started with. I both copied the
code and added in my own implementation so I was able to learn as I went along
with the steps. After going through the tutorial and adding a significant
amount of my own code, I hade a few questions I needed to ask Prof Ben. First,
I needed helping knowing how to handle with keywords in the parser, I had to
ideas of how to do this. Second, I was not sure how to handle arguments to
functions, where should I be hard coding in which arguments are required and 
which are optional? So, I stopped working for the night.

In class on Wednesday I was the first person to ask questions, and I learned a
lot. I learned that it is good to hard code the key words in the tokenizer (over
my other option of doing it through the parser) and that I should handle the
arguments in my compiler, not the parser. Prof Ben explained that the parser
should be more flexible than the language, and that checking arguments is like
doing type checking, and type checking is dealt with later!

After this conversation, I was able to complete a basic version of my parser
during class, and I continued to clean it up on Thursday afternoon. While
finishing this parser, I simplified by AST greatly. I know it looks more complicated
because there are more parts to it, but in reality the parts are much more
condensed than the original AST because my original AST was missing important
details/sections.

My original AST:
Type Pattern = [Element]
Type Element = Rule [Attribute] | Section
Type Attribute = String | Number | Function
Type Section = this is where we are going to have all of the different section types & their required and non-required arguments.
Type Function = this is where we will have the built in functions that take in arguments.
I also need to allow for comments in my code somewhere (where does this happen?)


My current AST:
Type Pattern = [Section or ImportSection] + GloalRules
Type GloalRules = "global_rule:" + Section
Type ImportSection = "import:" + Filename
Type Filename = a string ending with the characters ".cromd"
Type Section = { + [Keyword : Value] + }
Type Keyword = a string matching one of the hard coded keywords for the language
Type Value = Section | Argument
Type Argument = String | Number | Keyword | FunctionCall
Type FunctionCall = ( + [argument + ","] + )

Currently I have a parser that can read in my test file and properly parse it!
I feel that I am in a good place to go ahead and start working on my compiler.
While I have a list of things that I need to do to improve my parser, I think
it is in my best interest of saving time to work on the compiler first, because
a lot of things that I am worried about are related to the compiler or are
extra things that can be added on at the end (for example dealing with comments.)

My future concerns about the parser include:
* How do I deal with comments in the parser? I know that I will just ignore them,
but then go at the end of a line - is the regular expression just "#.*\n"?
* Is there a way I can make arguments not need "," after the last argument?

Next week I plan to begin by researching how I should write my compiler, and then
getting started on it! From here I think there will be a back and forth between
the two as I add more robustness to my parser.

## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

I need to figure out how to write my compiler! Where do I start? Within this, I
am going to need to make more final decisions on what the keywords are in my
language. How am I going to create PDF output? Should I do markdown output first
because that is easier?

**What questions do you have for your critique partners? How can they best help
you?**

I want to ask if they have any feedback on my parser, and what libraries they
are using for their own parsers. I also want to ask them what next steps I should
take, I am a little bit overwhelmed by starting the rest of my code.

**How much time did you spend on the project this week? If you're working in a
team, how did you share the work?**

I spent both classes and about 5 hours outside of class coding and 30+ min working
on my feedback.

**Compared to what you wrote in your contract about what you want to get out of this
project, how did this week go?**

This week went well, I did all of the review group related work that I needed
to do, and I made great progress on my project. I am happy that my parser is clean
and should be easy to use with my compiler. If I want to do some extra work to
be extra prepaired for next week, I should do some additional research about
starting my compiler. I might try to do this Monday morning before class as well.
