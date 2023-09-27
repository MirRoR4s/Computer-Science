welcome everybody this is the first lecture,

欢迎大家，这是 linux seven decal 的第一个讲座。

 on the advanced track for the linux seven decal,

i'm bernard and i'll be your lecturer for today and today we'll be talking

about sort of the general concepts that the

rest of the decal will sort of build on top of and that is

mainly unix and what linux is and how we interact with it so before we

dive into all that the first thing that i wanted to talk

about is just some of the administrative stuff

that you guys might find useful if you're watching this in a future

semester this may not be as accurate but

most of it still stands so as you all know

this decal like all decals has passed no pass in the past all you really need to

do is attend all the lectures watch all the

lectures um if they're online but attend them if we

have a guest lecture or something that's actually live

and turn it on the labs which are due one week from when this lecture actually

goes up um i believe the schedule here is that

this lecture should be coming out the first

thursday the class starts um because typically when the actual

lecture is in person these lectures happen at 8 pm uh at the

ocf lab itself but since we don't really have that

anymore we'll release these lectures when that time comes

and at the same time a lab will be released so

lab a1 should be on grade scope as well as on our website and you can get

started on that and that will be due in one week when

the next lecture comes out and the next lab comes out

so make sure to stay on top of things as in

for 10 weeks this stuff will sort of just be coming at you

on a weekly basis so we hope you enjoy it

all right so you guys might have already recognized me since i am a head

facilitator this semester as in i do handle a lot of

the logistics and those sort of questions are probably

best directed at me and ben but there's

probably also a lot of lectures that you may not have met before

who will be giving a lot of lectures you'll see for the rest of the semester

and while you may not know they're there or know them by name

all of us are reachable and online probably the best way to sort of do that

is to email us if you have something official um uh

regarding logistics or if it's something more casual or just

about the course content in general feel free to drop into any of our ocf

communication channels and jump into decal general and send us

a message there's a lot of ways you can sort of

reach us and we're always excited to sort of hear

what students are interested in if you guys want to help out at the decal

or if there's or if there's general feedback

or course content in the lab and lectures that you would like to see

changed

other than that all of our if you haven't looked at our website before

all the material from past offerings of this course can all be found there

as well as obviously the stuff that we're rolling out this semester

and lastly even though we won't be doing live lecture

since we can't exactly get every single lecture to be free at these times to

host these to host the lectures we'll still be

having office hours and demos in person when people can actually make them so

for example by the time this lecture goes up i

should be in this actual zoom room and you can jump in and talk to me or

ask me anything that you want to directly

i'd also recommend to pay attention to your emails

mainly because a lot of this stuff can be due to change whether that be our

course policy or a certain date and time of things coming

out um so and if we have any of those updates

we'll be sure to email everybody in the class before doing anything else

something else to also keep an eye out for is

if we have guest lectures or lectures that people want to give actually live

we may actually require people to tune in to a

a live lecture at the same zoom link but really just to make things easier

your first lectures we've been trying to have more of these lectures

recorded which i think also makes it easier for you students as well

so as far as engaging with this lecture we have a little short url here that you

can access and follow along with the slides

that i'm presenting today um hopefully this url will be updated by

the time this lecture goes live but it should point to the exact slides

that i'm showing right now i also recommend that you open your own

terminal whether it be on your own linux or linux or unix based machine

and if you don't have that you can just ssh onto

the ocf ssh server directly and run your commands there

and i also recommend to ask questions you won't be able to do that to me

directly but if you have something you want to ask you

can either jump into the office hours i'm hosting at the time

of this lecture dropping or you can just ask online

in our decal general channel which is meant for students

so what we'll be talking about today specifically

the title for this lecture is an introduction to unix introduction to

linux but really what we want to describe uh

in this lecture is really what those terms sort of mean

as well as the sort of ways that you may be interacting with linux

and things involving linux specifically so probably the most obvious example of

this is the shell uh if you're on the advanced track you

probably have interacted with the shell yourself

and have at least played around with it once or twice

but we'll go a little bit into the cool things that you can do

as well as uh the things that the shell actually makes possible

which may be a much bigger world than you may initially realize

and the lab itself will also give you a lot of practice with actually using the

shell as in that will be the applied part of this

topic we'll also be talking a little bit about unix

and the history of linux itself and we'll be looking a little bit at the

design decisions that made unix popular and the sort of things

that still make linux a very appealing option for

people today and lastly we'll be talking a little bit

about free and open source software that's all the stuff we'll be

interacting with is built on top of free and open source software

if it isn't for an open source software itself

and understanding the sort of community and development

that has come along with linux itself over the past few decades

so starting off with the shell

even though everyone here is on the advanced track

we can really just group all of you guys as sort of at

these three levels of understanding the first level is pretty simple my

favorite example of this is perhaps when you're starting out

working on a project or an introductory computer science or

data course you may get told to run some command

and you perform it and something happens and that's really as simple as

people's initial understanding of the show goes this is definitely my

experience when i first touched the shell

something like git clone repository definitely seems like magic when you

first run it as in you have this box of input you run this command and then boom

suddenly a directory and a bunch of stuff appears in it and really that's as

far as you need to understand things on the next

level we sort of have being able to use

programs to do what you want this can also be very simple running a

command like ls to see the sort of files and

directories in your working directory um is an example of wanting to do

something and knowing the program to actually execute it

but this obviously can get a lot harder depending on the thing you actually want

to do but you guys have probably probably all

worked at least with a few commands um that you sort of memorized

uh maybe good at performing individual different jobs

uh whether that be crap for finding specific things in input and at

a final level we have the ability to express much more

complicated behavior by putting commands together

manipulating output and sort of understanding as a whole

the sort of things that the shell can do for you

so now i'm going to dive into a short demo the intention which isn't exactly

to solve the sort of problems that you'll be seeing on your lab

or to do super complicated stuff in the shell itself

but really hopefully i'll be able to open your mind a little bit

as to what the shell can actually accomplish for you as well as maybe

helping you get a little bit more familiar with it

so jumping into that we have a list here of

a bunch of common shell commands um some of these may be very familiar with you

some really maybe a lot less so as well as a little bit of control flow

stuff that uh can be a little bit more advanced so i

don't intend to dive into all this sort of stuff

uh but i wanted to familiarize you guys with stuff that you may not have

already known about the shell but you perhaps have interacted with or touched

with before but never truly understood so let's jump into that

so in this demo i'm just going to sort of go through some of the shell commands

that were listed in the last slide i won't go too in-depth in each of them

but hopefully i'll give you guys some of the starting tools that you guys can

start working with so you have at least some basis for

starting out on lab a1

so as you can see here i'm currently just in my home directory

i'm running siege by the way but that shouldn't really matter

and we can see that if i type a command like ls i can see the files that are in

the current working directory that i'm already in this is probably something

that's pretty familiar to people that have

interacted with the shell before is the concept of the file tree that we

have to traverse i can use a command like bwd to see

where i am right now and i can see that i'm in my user home directory

great to move around we can go ahead and move into

a test folder that i've already made and we can look in here and see that there's

nothing currently in this folder so from here let's go

ahead and start playing around with some basic file operations and

sort of see with things that we can do we can go ahead and create an empty file

by using touch so we can make a file like

this and we can see that we created this file called bernard

now touch should create an empty file so we can go ahead and

list the contents of the file using cat and we see there isn't really anything

there

so let's go ahead and try to edit it there's a few common

terminal based text editors like nano and vim

you can really choose whatever you want whatever you find simplest but

they really all work the same as in the edit text within the terminal so let's

go ahead and open up this file this demo isn't really about how to use

vim and specific either i'd recommend if you're interested in something like that

to go look into something like vim tutor really here i just wanted to fill this

file with some random text

and there we go so now if we actually list the file consoles again we can see

that everything i've added to that file is printed when i run cad

all right

we can look at the head and tail commands we could look at head

so the next common command i wanted to show was head

which is supposed to show the first few lines at the head of a file

and by default it shows the first 10 lines and this is something that i

wanted to to change by passing an actual argument

for the hum for how many lines i wanted to show

but i ended up actually forgetting the syntax for the head command itself um

so what did i do i ran this command called man and

man is meant to show the man pages four commands

and show you a bit of documentation about how to use it so

what i did here was when running manhead i can see a lot of information

about how this command is supposed to work and

here i can see in the description that the dash and argument

is used to provide the number of lines instead of the first 10.

so that's great and running this command now gives us the first line of the

file that we just created entail if you if you haven't guessed already

really does like the same thing so instead of giving us the first line in

the file this now gives us the last

so far i was working with this small file that i created but perhaps this

isn't the best example um if we go ahead and look at the files in my

actual home directory we can see that i have

the text of moby dick in a txt file at my home directory so let's go ahead and

move it into this test directory which we can do

by the move command the move command like a lot of other

commands that interact with files all have a source argument and a

destination argument so in this case i want to move this file

which i can which is in the directory above the test directory which is my

home root directory and i want to move that into this

directory itself which i can do with this command

let me go ahead and look i can see that now hooray i have all the text of moby

dick and now when we run the head

[Music] the head command on this massive file we

can see the first 10 lines and we can run the tail file and also

see the bottom 10.

hooray but let's go ahead and try catting this entire file what happens

a whole ton of text comes out and this really sucks because

it's really really hard for us to scroll through all this and find anything that

we actually really want right this seems pretty useless so what

can we do instead if we sort of want to inspect

the contact the content of the file itself

well one command that we can use is less

so you can see when we open the file using less the contents of the file

are shown in our in our terminal but here we only see the first

section of the actual book itself to move through the file we can hit the

spacebar and the key b to move back up

and this is sort of all done from entering input in this sort of command

prompt we have here while the text of from what we see is

displayed up top

and there's a lot of cool stuff that we can enter in here the most useful one in

my opinion is pattern matching so we can use a backslash

we can use a pattern to search for a word like the then we can use keys like

n to move to the next iteration the next occurrence of this word and

also capital n to move back so this is pretty useful when we

actually want to find a text find a word in the text

so maybe we can try looking for something more crazy

maybe a word like boat

we can also press q to quit which is pretty common among a lot of shell

commands but let's say that we don't want to

actually look through the we don't want to actually search the text ourselves

what can we actually do to find words or find lines in this huge chunk of text

a very common command you guys may have heard of

is grep

again we can search for the word boat in this giant huge set of texts and we

can find all the lines in this actual book with the word boat

in it which is pretty incredible um and not to mention there's many other

options that grip has to do things a lot more complicated than

just searching for lines with that specific word so so far

i've been using these these commands by themselves but when

you begin to put them together you can start to do much more complicated things

for example the best example of this is piping which

you guys are probably all somewhat familiar with

we can go and pipe the content of one command

into the input of another so using commands that i've shown you so far

we can go ahead and grab the output of ls for a specific word

or i guess in this case letter let's go ahead and find

all the lines with the letter e in it and we can see that bernard comes up

but the moby dick text does not and this is probably the simplest

example of this that i can show but there's much more complicated things

that we can do next i kind of want to show off the said command which is a

stream text editor for example let's say in the moby dick

text we wanted to replace every instance of the word boat with something

else like let's say cat well then we can go ahead and print out

the content of the of the book itself then pipe that into

said from which then we can do something like

this

we can now see that all the lines that previously previously had the word boat

like a rocking boat are now rocking cat isn't that cute we can even make network

requests using basic commands in the shell

you guys may have heard of curl and we can go ahead and use it to

get the content at the main ocf website

and would you look at that it gives us a whole bunch of html

which is what we would expect from visiting the site directly

we could even save it to a file what i did here was redirect the output

of this command so normally when running curl this way

the content of this command will go to our standard output which is

why we see it show up in our terminal immediately after

running this command but using this arrow here we can redirect

the content into a new file that we decided to create there's

some pretty simple syntax and we can go ahead and look at the

content of this file to see that hey it's really

all there

so i know that i mentioned that i wasn't going to cover exactly how

every single piece of the show works but there's still some pieces that you

should probably know about so that you do have at least some

understanding of what's going on under the hood the question i want to answer

is how exactly does piping work and the answer to this involves a lot of things

every command that i provide to the terminal matter what it is

when ran spawns a process and you'll learn more about what a process

is in later lectures but just know that whenever these

processes are initialized they always start out with their own standard input

and standard output which are default file descriptors

which pretty much are streams of text that by default manage the input and

output of a program so when we do something like

using a program that has output

when we pipe it into a command that takes input

really it's as simple as redirecting the standard output of one

to the standard input of another now underneath the hood

something like a pipe will actually allocate a page and a whole bunch of

other stuff but just know that these systems sort of

exist and this will be expanded on a lot later

writing and using a function in the shell is a feature that probably most of

you have never really used before but i think a simple function like this

serves as a good example as to how these commands and functions

consume and output pieces of text like any

command that we've used previously hello in this case can be called with a

set of arguments for example i can provide my first and

last name and the text i provided will be printed out in when the function

is ran because the dollar sign 1 and dollar sign two variables here

correspond to the first and second argument of the function that it was

just ran more commonly you'll see these sort of

functions in shell scripts where people will write operations that

can be performed in the shell into a file all of the commands i've run so far

also have something called an exit code this code

is meant to tell us whether or not the last command was successful and we can

access it by looking at the dollar sign question mark

variable in this case the execute that we have is

zero which indicates success

and that makes sense because the script above succeeded in printing the input

that we wanted but let's try something else

let's try a command that will obviously fail like for example let's try to

move directories in a directory that doesn't actually exist um

something like this and you can see that when we actually look at the

exit code it is no longer zero indicating

a failure using the exit code we can do some pretty cool stuff

for example we can chain commands only if the first the previous command

was successful for example we can list all the files in

our directory and then

we can say hello and we'll see that these

two things ex execute one after another the ants the ampersand symbols i use

here indicate the and if operator so if i were to do

something similar to before where i try to move into a directory

that doesn't exist but then and try to do something

if and only if the last command succeeded

we'll see that the second command here doesn't actually execute

so now that you guys have seen some of the cool stuff we can do in the shell

and some of the commands that we can invoke and how we can put some of them

together we can now take a look at how all this

is put together into things like small shell scripts

so as an example i've already created this script here called fibonacci so we

can go ahead and take a look at that

and you'll instantly notice a bunch of different things about this script and

i'm just going to go through these things individually

so at the start at the top of the script we see something that's called a shebang

and while this does look like a comment just like the line below it

the idea here is that this line should tell your interpreter

what it should use to actually run this script

when i say shell script i really mean a script that's written in a shell

language like bash but in reality these ship bangs can specify all sorts

of languages like python as a way to run a script the next thing

you might immediately notice is some of the syntax

that this script involves we see things like if

then phi exit all of these keywords sound like things that control the flow

of how this script actually runs and you would be correct

in fact it may look similar to other programming languages that you've

interacted with so the first thing that we see here is

an if statement the if here as expected pretty much controls whether

or not we enter this block of code inside of here or not and it ends with a

phi which may not immediately seem logical

but we close an if statement with if

reversed then we can take a look at the sort of

statement that we are evaluating in this case we're asking whether or not

this dollar sign pound variable is equal to

zero this may seem confusing as in there's no actual command here being run

that's testing equality but these specific brackets are actually

running something called the test command under the hood

which is meant to test equality the dollar sign pound argument here

specifies how many arguments have been received

so it makes sense that if this value is zero then this fibonacci script hasn't

actually received an argument and we exit

with a non zero status code meaning that we errored

below that we see the fibonacci function which looks pretty similar to the hello

world function i showed earlier now i'm sure you all can guess what this

function actually does but seeing how it does it is the interesting

part we start with a statement where we assign

dollar sign one to this variable n dollar sign one is our first argument so

in this case it would simply be the number of the fibonacci number that

we want to find the statement below is another if block

which checks whether or not the argument that's passed in is a

positive integer as in fibonacci doesn't really make much sense

without one and while the statement seems sort of

complicated again the if statement uses the brackets

and some more complicated logic to get this done

below that we have some more control flow statements with if alif

and else statements then look at some base cases of small fibonacci numbers

and then a very interesting line here at the bottom

so if you haven't guessed already this function here seems to be recursively

calling itself to actually find out what the nth fibonacci number is which

is really cool it's amazing that something that you

might find in normal programming language can be expressed in

the actual shell that you're working in and there's a few quirks that i want to

point out here there's a whole mess of parentheses in this line

but the ones that i want you to pay attention to are how sometimes one

follows a dollar sign and sometimes two of these parentheses follow a dollar

sign in bash the double parenthesis and

dollar sign is a mathematical evaluation of the statement inside

so even though the variable n which is the argument passed into the script

is in fact text its value will be evaluated mathematically

within these parentheses on the other hand we have this fib

statement with an argument following it that's inside a statement with a dollar

sign and a single parenthesis in this case that statement is actually

going to be evaluated and the value it returns will be the

actual result and lastly we see that we call this

function with the argument provided to the script

to kick off this entire recursive process

so while this does seem pretty magical i hope you can also see how this seems may

be a little bit overly complicated not having integer types makes this sort

of logic hard and implementing this in a language like

python would probably be a lot easier but nevertheless i just wanted to

demonstrate that a lot of the typical behavior you might

find familiar in a programming language can often be expressed in the shell

which makes it very very powerful so onto a script that maybe is a little

bit more realistic to what you might find in the real world

so here i have this script called sync archive this script brings back a lot of

memories because this is one of the first

contributions i ever made to the ocf which was

modifying and creating this script for our

mirrors service the ocf mirrors software which means we host a copy of open

source software like arch linux in this example

and distribute it to people who are closer to us so that their downloads are

faster the overall context of the script is

that we want to make sure that the copy that we're hosting is up to

date with the upstream source and while i won't go into the exact

behavior behind every single line of this script

there's two important things that i wanted to point out one is that again

pretty complicated and expressive behavior can be

expressed in a simple shell script we see that in this line here

we're checking with curl to see the last update time

of arch linux and then we see the difference between that

and when we last updated our mirror and then from there perform the correct

behavior in the case that a new update is necessary second there

may be syntax in the script that even people familiar with shell scripting may

not immediately recognize for example this line here we substitute

and execute this command is something that's actually very unique to bash

these things are traditionally called bashisms which are pieces of behavior

unique to bash and can make your life a lot easier but the thing i wanted to

point out here is how not all shells are the same writing

lines like these or using the double brackets in this line may not give you

the same results depending on what shell you use which

again all calls back to how important the shebang at the top of the file

really is and while a lot of this syntax may look

very complicated or intimidating at a first glance

i'm confident that with your guys google skills reading and developing these

shell scripts is really just a matter of knowing where to put what but i hope

i've sort of showed off some of the cool things that can be done

so now we can jump into a little bit about the history and core concepts

behind unix and linux and hopefully clear up some of the

confusion behind a lot of this terminology in general

i feel like unix linux uh gnu and all these things

seem uh like just terms that you may have heard of relating to a lot of this

sort of stuff but you also may not understand how

these pieces all sort of fit together so i'm gonna go ahead and dive a little

bit into that

um so unix as an operating system started out a long long time ago in the

1960s when bell labs and mit worked together

to make this operating system called multix

which was meant to have all these really cool you know features

and things like multi-processing and it ultimately

didn't pan out but one of the people who worked on this ken thompson

took a lot of the great ideas from multix and other operating systems at

the time and put it all into unix which is

a project that sort of sought to have a lot of those same features

but with a lot less complexity and with a much more

simpler developer friendly design and those sort of things made unix very

popular in the coming years and many other derivatives like bsd

solaris other operating systems uh grew as sort of forks and offshoots

of unix itself and from then on unix only grew in

popularity even with things like bell labs breaking

up and att being formed didn't stop munix

from growing in popularity and a lot of the legal troubles that

surrounded unix and its sort of offshoots

inspired the growth of linux which was a copyleft rewrite of unix

which is the main way that we interact with unix today

and linux nowadays is a very popular operating system

the final bullet point is a bit of a joke as in if you know anything about

linux its popularity isn't exactly in the

common desktop that people use but

servers today around the world are all primarily running linux

and that's why it's so important assist admins uh

to know a lot about linux as in most of the servers we interact with and

administer are all running linux nowadays so from

that short gist of unix and linux's history um

i hope it's clear that the main distinction from linux

and its unix history is really the idea that it is truly free software

as a copyleft version which i'll dive a little bit more into later when we talk

about free and open source software uh but the movement behind it and the

software itself are pretty inseparable you may be wondering what gnu stands for

one that has to do with linux and in short gnu actually really is the

operating system we call linux so the terms are used pretty

interchangeably nowadays even though in specific linux refers to the kernel

but gnu as an acronym stands for gnus not unix

which is a funny sort of recursive acronym

but it serves to show how linux itself was meant to be very separate from unix

although by design it is very similar and

the main difference here is the fact that gnu and linux are free software

unlike unix and the legal troubles that faulted in its history

that's not to say that linux as we know today is the only relevant offshoot of

unix you guys may have heard of bsd before a

unix derivative from berkeley go bears mainly because of

the important things that bsd implemented and are a core part of the

operating systems that we know today features like berkeley's networking

sockets are things that are pretty much present

on all operating systems nowadays and we can really thank bsd for implementing

that while people don't really run bsd itself

nowadays if you're running mac os uh you are

running a bsd derivative so at the end of the day it all trails

back to unix

so this is supposed to be a graph of unix's history over the past few decades

um and at least for me i don't even recognize half the terms

on this chart but it really goes to show how the ecosystem of operating systems

that has sort of spawned because of unix and how that sort of affected

a lot of the software that we interact with today

yeah pretty cool stuff

so now that we've seen that unix has had a long long history

we have to sort of ask ourselves what part of unix has sort of maintained its

popularity as software over all these decades

and what about it makes it still relevant for us to talk about today

at a high level really all of the design decisions made back when unix was first

designed are still very very relevant today when

i talked about how ken thompson originally designed the

operating system to be generic and very simple that proved to be very

appealing for developers as the simplicity of the software itself

made it very simple and almost fun to interact with

as you may be sort of saw in my shell demo and you definitely will see in our

lab a lot of the features that unix has even

in the shell with its with its commands that do very simple

and individual things can be pieced together to do really

really complicated and impressive things as a larger program

and this sort of all goes back to unix's original philosophies

where all of its software is supposed to be simple modular

and do one thing and one thing only very very well

and this philosophy has definitely persisted around unix

and has been the topic of a lot of debate

around newer and much more powerful tools that

have become a part of the sort of linux ecosystem if you know anything about

systemd you may be able to see ways in which

when thinking along the lines of this philosophy

monoliths like systemd can seem like antithetical to the original design of

unix and how unix was intended to be used

and lastly you may have heard that in unix everything is a file

um and while this doesn't actually mean that really everything

truly is a file the concept here is that the apis that people use to interact

with files the syscalls that they use to read and

write to files have been heavily reused in a lot of

other things in the unix ecosystem like device drivers and

stuff like that which brings down a lot of the overhead

to writing custom software when you can abstract a

lot of the ways of interacting with things

as if everything was a simple file with permissions

and as a stream of bytes

so diving a little bit more into that you may have heard of the syscalls

to interact with files and these are pretty obvious from a high level that

you should be able to read the files write to files and open files

but these functions in unix also provide a pretty generic way to interact with

things that aren't just files as in anything that's a sort of stream

of bytes can be tied to a file descriptor and things

like sockets drivers pipes et cetera et

cetera and this really simplifies the design of

a lot of these things as in the things that you may find natural

about files themselves already apply to other pieces of

software the big ones here are things like

permissions and because of that all the examples

listed here also have their own permissions and access control

and things that you would find familiar on files themselves

so knowing all this it becomes sort of clear the advantages unix has over

systems that maybe don't abide by these philosophies

a lot of the software that is a part of unix is a lot easier for developers to

understand because in a way the software is dumber

and the software is simpler i also cannot emphasize enough

how unix is very very friendly to developers

let's say you want to debug something or see what's going on really in your

system things like proc fs which is a file

system sort of delineating all the processes that are

working on your system and s-trace a way to sort of trace the syscalls that are

going in and out of your kernel are all examples of features that have

all been a part of unix for a very long time

and allow developers to sort of see very very closely into what

your unique system is actually doing which as you'll see through the rest of

our labs can be very very useful we have this

funny quote here from bill joy who was originally tasked with

implementing tcp and ip on berkeley unix and while this quote is sort of an

exaggeration i like to think that this quote does sort of show

how simple extending software on unix can really be

so now i have to talk a little bit about free and open source software

and while i've already been bringing up these sort of terms when i was talking

about the history of unix and linux itself

the concepts of free and open and licensing are all things that

while they may not be immediately applicable to you and what you intend to

do with what you learn in this decal are really

important to really all the software that you'll be interacting with this

entire semester

so to begin with we have a strange question that we need to answer in the

first place which is what is free software um so right away

i'll tell you free software doesn't exactly mean free as in

free of payment but rather it's a sort of question about intellectual property

when you write software when you write the code who owns it

uh you know what does it mean to own code in specific

um does that mean that you have the exclusive rights to use it

does that mean that you're the only one who can distribute it

does that mean that someone who copies your code can be sued

really this is a whole host of questions that that begins to sort of cross the

border into more moral and legal questions more than

anything else there's maybe a few terms that you've

already heard me bring up and i'd like to at least define some of those

at the top of this slide we can also see a scale of the

freeness of different licenses for example you may be

familiar with open source which as you guess is pretty free

as in you have access to the source code but we also have

licensing that's even more free which we'll talk about a bit more later

like copy left and other things like closed source code are a lot less free

as in the source is not something you should be able to

see at all i guess at this point we should also

sort of dive into what the definition of free and free software

really does mean the free software foundation has given

us these sort of definitions and you'll find that most of these

tenants sort of answer the questions about code ownership

that we had in the last slide for example we have the freedom to run your

program we have the freedom to study how the

program works by having access to the source code

we have the freedom to redistribute copies of the actual code itself

and we have the freedom to also modify and distribute

code so with that framework in mind let's look at a very very common license

that's pretty commonly seen on a lot of github repositories and open source

software today which is the mit license and if you want

to read this you can just pause here or just google

more about the license online but it seems pretty short and pretty succinct

and the main reason for this is the mit license is a bsd like license as in

it's a permissive and simple license that really just says you can go ahead

and use our code but just don't sue us and respect our

patent rights and really that's about it and the

simplicity of this license is part of the reason why it's so

popular as it really just says hey this is open source and really that's as

far as this licensing goes so for a more complicated

license the gnu public license uh is a little

bit different so again you can pause it if you want to

sort of read this but jumping on into this this is what i

originally referred to as a copy left license so while the mit

license sort of says that hey this is open source and you can do whatever you

want with it the idea behind the copyleft license is

that if you intend to build off of this code

and uh let's say develop your own fork and build the top of the original source

that iteration that you produce must also have

this same copyleft license and from there it has this sort of

viral effect as in any software that has grown off of

code starting with this copyleft license will also continue to do so

as the software continues to grow an example of this is

let's say there is some open source piece of software that

i want to work on and let's say that i take a

huge chunk of the source code to build my corporate product

and that i can then treat as closed source

that would perfectly be fine if the code was from an

uh if that code had an mit license as in i can really do whatever i want with it

and in this case i've now transitioned my own code that has now worked on top

of it into its own closed source version

however if i intended to do something like this

off of a code that has a copyleft license like

the gnu license suddenly i'm in a very different

situation where i cannot build on top of this code

and also make it closed source and a great quote here from the very

famous steve ballmer is that he called this license a cancer

that attaches itself in an intellectual property sense to

everything it touches which uh is a little abrasive but

honestly pretty descriptive as to how this

license is attended intended to work so lastly i've talked a lot about the

concepts of free and open source software

um but you may be wondering why go through all this trouble in the first

place why are we talking about free and open source software at all

and really the main reason behind this is without freedom

of open source software there really isn't anything there wouldn't really

have been anything for us to talk about today in

the first place all the software that we've interacted with today

and probably almost all of the software that we'll be interacting with

for the rest of the semester is all built on top of or is free in open

source software even at the ocf everything that we run

all the code that we write all the services that we deploy are all

free and open source and there's many reasons as to why free

and open source software has become so popular

over the past few decades there's some reasons listed here

and i'd like you to sort of just think for a second about how free and open

source software can help you in each one of these sort

of categories firstly free and open source software

from a monetary standpoint really is free

um as in if you have access to the source code you can run it you can

build it and run it yourself and you don't really have to

and you avoid the entire cost of needing to write

code from scratch not to mention the ability to

have a community of people who will continue to maintain software

as time progresses which is very easy to see

with examples like linux which has now had a life of decades on decades

on the hand we can look at security and in the case where things are open source

and people can view the source code directly it may be a lot easier for

people to find bugs and security in critical pieces of software if

the code is open and available for people to simply look out and try to

debug

from a privacy standpoint the transparency of having open source

software again allows people to sort of look into the

code and ask questions about what software may be doing in regards to your

own privacy control is also a major factor as maybe

there is some feature of some free and open source software

that you don't like well no one's stopping you from forking the software

and building your own version without it or with different features

and this is something that's pretty commonly done in the ecosystem of free

and open source software and lastly and probably the most

importantly we have collaboration as in all of the pieces of free open

source software on the slide really could not have been

done with an individual person but because of the fact that the code is

free and open source the barriers for people to collaborate and work

together on stuff really is very very low you don't have to be in

the same company you don't have to be even in the same

country but really everybody has the ability to view

and build on top of the code that is publicly shared in open source

finally we have a small note on terms this is stuff that the original

creator of this lecture wanted to mention and i'll let you pause it here

if you want another reminder clarification about what these actual

terms specifically mean

but really that's all i had today um thanks everybody for

following along um we have some resources on this slide

and while you won't be able to click on them in this recorded lecture i

recommend that you open these slides using a link on the website or the short

url that i mentioned earlier to look into some of these if you're

interested in learning more about the history of unix

or just some more generic stuff to make yourself a better linux user

but other than that thank you everybody for following along and have fun working

on the lab