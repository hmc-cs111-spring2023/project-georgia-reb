# Design notebook entry

## Last week's critique

**TODO:** Fill in this part with a summary and reflection on the critique you received for
last week's work. Answer questions such as:  How, specifically, did the feedback help
improve the project? Did the feedback point out or offer something you hadn't considered?
Did it help you make a design decision? Was it helpful in addressing the most pressing
issues in your project? How will you incorporate the feedback into your work? Will you
change something about the design, implementation, or evaluation as a result?

In class, I mainly asked what my partners thought about the readibility of
the language and my documentation.

The main feedback and ideas that I recieved was to make the language
in my documentation more accessible to crochet users (don't use CSy terms like
"pass in") and to add output images to the examples in my documentation. I
think these are great ideas and hope to implement them next week!

In my feedback from Kate, she gave me suggestions about fonts in LaTeX, which
was motivating for me to go look up myself, and she re-iterated the idea about
using accessible language. This feedback was helpful and motivating for me to
finish this project!

## Description

**TODO:** Fill in this part with information about your work this week:
important design decisions, changes to previous decisions, open questions,
exciting milestones, preliminary results, etc. Feel free to include images
(e.g., a sketch of the design or a screenshot of a running program), links to
code, and any other resources that you think will help clearly convey your
design process.

My goal for this week was to finish the main implementation of my code, so I
can spend the remainder of the time next week finishing the documenting, final
packaging of the code, and the video example. I have been able to do this!

During class on Monday, I made myself a todo list. It includes:

1. Finish abbreviations on the project details page
2. Pattern section page
3. Assembly page
4. Add more global rules
    1. Font type
    2. Font size
    3. Font color
    4. Background color
5. Allow comments
6. Make it so you don’t need the last parenthesis in the parser
7. Changed the way that we carry the file

I think got to work! I finished up the abbreviations on the project page, and
have allowed users to write their own abbreviations or use a function that
writes them using definitions from an official looking crochet website. I think
this will save users a lot of time, but also give them their own flexibility to
write additional rules. If a user really wanted to, they could also go into the
source definition code and update the definitions to be their own (but that is
not really a part of my language).

I then created the pattern section and assembly pages. These pages a almost
identical, except for the header formatting. I think that I came up with a clever
way to do lists as well. For a list, you can either add just a text item, or
you can add items which contains text and how many times that line will be
repeated. I think this both makes it so users don't need to be bogged down by
writing out the line numbers themselves, and I can easily format line numbers
like `3-6` which is common in crochet.

I then went back and added more global rules. I ended up not adding fonts,
because it is frustrating to understand what fonts are out there for LaTeX, so
this is something I would add with extra time at the end. I first figured out
how to change all of the text colors. I then realized that I wanted more flexibility,
so I allowed users to edit the background color, and the heading and text colors
separately. I also created three font size schemas, small, medium, and large,
and for each of these set LaTeX font sizes for the title, subtitles, and the
regular text.

At some point I made sure to add all of the constant lookup values into a
separate [cromdDefinitions.py](https://github.com/hmc-cs111-spring2023/artifact-georgia-reb/blob/main/cromdDefinitions.py)
file so they can be stored together and easily edited.

While I was nervous about adding comments, it ended up being very easy. I used
the regex string I have brainstormed earlier, `"#(.*)\n"` and read online that
the comments should be removed in the tokenizer. This made so much sense, it is
exactly like removing the whitespace! So, I did that and it worked super well!

While I was working on all of this coding, I realized that I had an inefficiency
with how I store the output file IO object. I had been passing it through to
each method call, which is very unnecessary. Therefore, I changed all of my
code to instead store the file type as an attribute of the class.

After all of this was done, I again made myself a list of the things that I have
and haven't completed so far.

, this one
for both this week and the future. This list includes:

* Fix the image stuff
* Global rules are completed
    * The only idea to add is a font, but this required understanding the LaTeX font options
    * API is done too
    * Should I move the global rules to the start of the document rather than the end?
* Import is done
* Title page
    * Only thing to add is a copyright section
* Pattern details
    * I should add some links to basic tutorials into the text!
    * What do I do if a user wants to add a link to a section? 
    * Should I switch to a text and link option?
* Pattern section
    * Confirm what image types LaTeX takes
    * Work on the image size options
* Assembly
    * Same as for the pattern section
* Code overall
    * Add more comments to the code
    * See if I can remove the extra `,` at the end of things (or if that messes everything up)
    * Figure out how to package the code so that it is most usable for a user
    * Write the empty starter file
    * Clean up the pdf output creation so it doesn’t print all the crap
* Documentation
    * Finish API page
    * Cleaning it up
    * Writing overall information at the top
    * Write the home page
    * This includes creating a better title!
    * Write the getting started page
    * Add image output examples to my documentation!
    * Change language in the documentation to be more crochet user friendly?

I fixed my image problems, updating the image types in the API and allowing a
user to determine the size of the image. This completed the pattern section
and assembly problems as well.

I decided that the pattern details problems are something I can add if I have
extra time at the end.

When working on adding the copyright section, I realized that I am not sure how
others would write copyright, and that I should be allowing the users more
flexibility anyways, so I instead added a generic text section. This thought
inspired me to add the text and space parameters to the pattern section and
assembly pages as well, which I did.

Therefore, at this point I have mostly completed my code, what is left is the
final packaging of the language and documentation, and adding extra things if
I suprisingly have extra time this week. I am very happy with what I have
completed, I think this project is turning out well!

Extra: I came back on Thursday night and worked on the documentation. I added
a step through introduction page, and I added images to the wiki.

## Questions

**What is the most pressing issue for your project? What design decision do
you need to make, what implementation issue are you trying to solve, or how
are you evaluating your design and implementation?**

My most pressing issue is figuring out how to package the code so that it is
easy for users to download and to write about this process in the API. How do
I package the python code to compile a cromd file in one command? Once I do this,
how do I create a user tutorial on my wiki?

**What questions do you have for your critique partners? How can they best help
you?**

How can I make my documentation most accessible to users? They can help me by
letting me bounce ideas off of them.

**How much time did you spend on the project this week? If you're working in a
team, how did you share the work?**

I spent ~5.5 hours on Monday afternoon and evening, as well as ~1.5 hours on
Tuesday morning finishing coding and writing this notebook. I also spent
about an hour on the project on Thursday evening.

**Compared to what you wrote in your contract about what you want to get out of this
project, how did this week go?**

I am super excited, and think I am doing well. In my contract I wrote that an A
project would include through documentaion, and I have started to do that and
left myself plenty of time next week to continue the documentation. This week
went very well!
