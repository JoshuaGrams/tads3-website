---
title: Adv3Lite - Quickstart
description: A guide for quickly starting a new adv3Lite project.
published: false
---

# Adv3Lite Quick Start Guide

Welcome to adv3Lite! This Quick Start Guide is designed to get you up
and running as quickly as possible. It contains three sections:

1.  Instructions on [installing the system](#installing) and creating
    and compiling a minimal game (as a basis for further work).
2.  A guide to the [other documentation](#documentation) to help you
    choose which manual to look at first and which you can leave till
    later.
3.  Instructions on creating a [sample game](#sample) for people who
    want to leap right in and try out something hands-on before starting
    to read the other manuals.

Enjoy!

## 1. Installing Adv3Lite and Creating a Project

### 1a. Windows Users: Installing and Creating a Project in Windows Workbench

1.  The adv3Lite library comes in a zip archive containing an adv3Lite
    folder/directory and a number of subfolders. A good place to unzip
    this into is the extensions folder/directory under the
    folder/directory in which you keep, or plan to keep, your TADS 3
    game source code. On a Windows system this will typically be under
    My Documents\TADS 3; the TADS 3 author's kit setup program should
    create both this folder and the extensions folder under it. On a
    non-Windows system you may need to create these directories manually
    yourself. You should therefore end up with all the adv3Lite material
    in a folder somewhere like ...\My Documents\extensions\adv3Lite
    (where ... is the path to your My Documents folder or its equivalent
    on a non-Windows system). If you need to reinstall adv3Lite (for
    example, because you want to update to a newer version) I recommend
    that you first delete the existing extensions\adv3Lite
    folder/directory before unzipping the new adv3Lite folder to the
    same location; this should avoid any problems that might arise from
    remnants of an older version interfering with the newer version..
2.  If you're using Windows, run TADS 3 Workbench (by selecting it from
    the "Start" menu group you selected during the installation
    process).
3.  The first time you use adv3Lite, select Tools -\> Options from the
    Workbench menu. Scroll down to the System -\> Library Paths section
    of the dialog box that should then appear. Add the full path to the
    directory where you installed adv3Lite (e.g.
    C:\Users\Eric\Documents\TADS 3\extensions\adv3Lite) to the list
    (click the Add Folder button and navigate to the folder you want and
    then select it). You may need to close Workbench and reopen it for
    the change to take effect, but once you've followed this step once
    you shouldn't ever need to do it again (at least, not on the same
    machine, assuming you don't move things around).
4.  By default, Workbench will show you a "welcome" dialog asking you if
    you want to open an existing game or create a new one. Click on the
    button for creating a new game.
5.  If you've turned off the "welcome" dialog, then select "New Project"
    from the Workbench "File" menu.
6.  In either case, this will display the New Project Wizard. Just step
    through the wizard screens to tell Workbench the name and location
    for your new project files. Workbench will automatically create all
    of the necessary files for your project, and it'll even compile it
    for you right away.

The steps you'd typically follow once the wizard is launched would be:

1.  In the dialog that should then appear, simply click **Next** to
    continue to the second page of the Wizard.
2.  In the second page of the Dialog, type "Burglar" (without the
    quotation marks, and using a name appropriate for your own game if
    it's not "Burglar") in the upper (**Project Name**) box, then click
    in the lower(**Folder location**) box. From there you can select an
    existing folder, but for a new project you should create a new one,
    so click the **Make New Folder** button and then enter a name for
    your new folder, such as burglar (making sure you create it under
    the ..\My Documents\TADS 3\\ folder). Then click **OK** followed by
    **Next**.
3.  In the third page of the Dialog, scroll down the list of Project
    Types until you get to **Adv3Lite**. Click on Adv3Lite to select it
    and then click **Next**.
4.  Fill in the information on the final (Bibliography) page of the
    wizard (e.g. with the name Burglar, your own name and email address,
    and a brief description like "A small tutorial game") and then click
    **Next** to complete the wizard. Your new adv3Lite game (or at least
    the beginnings of it) will then be created for you.
5.  Wait until TADS 3 Workbench has finished created and compiling the
    new skeleton game (you should see a message saying 'Build
    successfully completed' followed by the date and time). In the
    left-hand pane of Workbench (headed 'Project') look for the section
    (near the top) that says 'Source Files' and double-click on the icon
    representing the file you asked the Wizard to create at Step 3 above
    (e.g. 'MyNewGame.t'); it should be the third one down. You will then
    see your new game source file open in the Workbench editing window.
6.  To compile the project again when you've made changes to it, just
    press the F7 key. (You can also select the "Compile for Debugging"
    command on the "Build" menu, or click the equivalent toolbar
    button.)

1b. Installing Adv3Lite and Creating a Project Manually (for non-Windows
Users)

If you're *not* using Workbench (which at this stage should only be
because you're not using Windows), you'll have to create your project
files manually. Fortunately, this isn't very hard - you just need to
create two files and one subdirectory.

To set everything up to create a new game (which we're calling "Burglar"
in preparation for the next section, although the same principles apply
whatever you're calling it) carry out the following steps:

1.  This assumes you've placed the adv3Lite directory under an
    extensions directory under your TADS directory, and that you'll
    create your Burglar directory in the next step under the same TADS
    directory.

2.  Under the directory you've created to hold your TADS 3 source code
    (you might have called it TADS 3) create a new directory called
    Burglar.

3.  Locate adv3Lite/template directory and copy (don't move) its entire
    contents (but not the directory itself) into your newly-created
    Burglar directory.

4.  Navigate back to the Burglar directory.

5.  In the Burglar directory, rename the file **adv3Ltemplate.t3m** to
    **burglar.t3m**.

6.  In the Burglar directory, delete the file
    **adv3Ltemplate.tdbconfig** (if you're not using Workbench, you
    don't need it).

7.  In the Burglar directory, create a subdirectory called obj (if it
    isn't there already).

8.  Now open the burglar.t3m file in a text editor and edit it to
    read:  

             -D LANGUAGE=english     
             -Fy obj -Fo obj
             -o burglar.t3
             -lib system
             -lib ../extensions/adv3Lite/adv3Lite
             -source start
                                    

    You can delete any instances of comments like the 'warning ' this
    file was mechanically generated' paragraph you find in the t3m file,
    together with any bits of executable code you find there. You can
    also delete the line -pre. You may need to change the penultimate
    line if the path to where you've stored the adv3Lite directory is
    different from that assumed here.

9.  Open a Terminal window. The Terminal program is located in
    Applications \> Utilities. You may want to make an alias for it and
    drag it into your Dock.

10. In the Terminal, use the cd (change directory) command to navigate
    to the folder where your game files are stored. For instance, you
    might type 'cd Documents/TADS/Burglar' and then hit Return.

11. While the Terminal is logged into this directory, you can compile
    your game using this command:

             t3make -d -f burglar
                                    

    If all goes well, you should see a string of messages in the
    Terminal window, and a new file (heidi.t3) will appear in the
    Burglar directory. This is your compiled game file. If you've
    installed an interpreter program that can run TADS games, you'll be
    able to double-click the .t3 file and launch the game to test your
    work.  
    Alternatively, you can run the game directly in the Terminal by
    typing 'frob buglar.t3' and hitting Return.

12. Keep the Terminal window open and press the Up arrow on the keyboard
    each time you want to do a compile, as this will reload the last
    command line that you typed (t3make etc.).

### 1c. Running Your Game

If you're running Workbench, once again, this is easy - press the F5 key
(or select the "Go" command on the "Debug" menu, or click the equivalent
toolbar button).

If you're not running Workbench, at your system command prompt, type

       t3run mygame
                        

But you should check the README file that came with your system's
download package - the program name might not be the same everywhere,
and of course you should replace "mygame" with the name you actually
gave your game, such as "burglar".

## 2. Where to Go Next: Navigating the Documentation

Adv3Lite comes with a number of different guides and manuals. Which of
them should you start with?

The first thing to be aware of is that two of the manuals are intended
as *tutorials* (for use when learning TADS 3/adv3Lite) and three are
intended for *reference* (for use when writing your own games once
you've mastered the most common features of Adv3Lite). There is overlap
between the contents of these two groups of manuals, since you may well
want to use the reference material to remind you of material you first
encountered in a tutorial, but they have quite different functions.

The two *tutorial* manuals are the [Adv3Lite
Tutorial](tutorial/index.htm) and [Learning TADS 3 With
Adv3Lite](learning/LearningT3Lite.pdf). If you're already reasonably
familiar with TADS 3 (but want to find out about Adv3Lite), you could
probably skip these tutorials and go straight to the [Adv3Lite
Manual](manual/index.htm). Otherwise, you should probably start with one
of the introductory tutorials. So why are there two introductory
tutorials and which of them should you choose?

There are two because people have different learning styles and
different needs and come to a system like TADS 3 from different
backgrounds and with different previous knowledge and experience.
Different people will therefore benefit from different approaches.

For most new users the answer to the question "Where do I go next?" is
either the [Adv3Lite Tutorial](tutorial/index.htm) or [Learning TADS 3
With Adv3Lite](learning/LearningT3Lite.pdf). If you're still unsure
which to start off with, take a quick look (by skimming) through the
first couple of chapters of each and then choose the one you feel more
comfortable with.

### 2a. The Adv3Lite Tutorial

The [Adv3Lite Tutorial](tutorial/index.htm) walks you through the
creation of three adv3Lite games (two very short, one quite a bit
bigger), explaining features of the system as it goes along but not
presenting them in a particularly systematic fashion (the order of
presentation is dictated by the order in which the games are developed).
Completing the tutorial will introduce you to the process of writing
Interactive Fiction in TADS 3/adv3Lite and in doing so will introduce
you to many of the features of the system. It is the manual you should
begin with if you prefer a hands-on, inductive learning style or if you
feel more comfortable being walked through the creation of a couple of
games before trying to branch out on your own.

### 2b. Learning TADS 3 With Adv3Lite

[Learning TADS 3 With Adv3Lite](learning/LearningT3Lite.pdf), on the
other hand, takes a far more systematic approach, and aims to introduce
you to all the most commonly-used features of TADS 3 and adv3Lite. It
makes no attempt to walk you through the creation of a game, although it
does provide a number of exercises you can try out for yourself (in the
form of descriptions of mini-games you can try to write together with
heavily-commented sample code you can download to compare with your
efforts). This might be the tutorial manual you would choose to begin
with if you're reasonably confident about programming or writing
Interactive Fiction in another system and you want to see how it's done
in TADS 3, or if you prefer to be introduced to the material in an
orderly, systematic fashion and you don't particularly need or want to
be hand-held through the creation of a couple of tutorial games.

### 2c. The Reference Manuals

The three *reference* manuals are the *Adv3Lite (Library) Manual*, *TADS
3 System Manual*, and the *Adv3Lite Library Reference Manual*. These are
the three manuals you will probably find yourself consulting most
frequently once you have mastered the basics of TADS 3/adv3Lite from one
or more of the tutorial manuals and are writing your own game(s), but
for most people, they are not the best place to start.

That said, the [TADS 3 System Manual](sysman.htm) does contain a lot of
material that might be of interest to confident beginners with a strong
programming background (whether professional, amateur or hobbyist) who
want to see how things are done in TADS 3, and the [adv3Lite
Manual](manual/index.htm) does contain a fairly complete and systematic
account of the features of the adv3Lite library, which could be a useful
place to start for people who know TADS 3 but what to find out about
adv3Lite. Nevertheless, for most new users of TADS 3 these two reference
manuals will not be the best place to start; for one thing in addition
to the more basic information they cover, they both contain quite a bit
of more advanced and complex information that is likely to be not only
unnecessary but also potentially quite confusing to new users of TADS
3/adv3Lite. You will also find the [Adv3Lite Library Reference
Manual](libref/index.html) an absolutely essential tool once you start
working on your own games, and *Learning TADS 3 With Adv3Lite* will
introduce you to its use, but it's certainly not the place to begin.
Please be assured that you absolutely do *not* have to master the
material in these three reference manuals in order to start using (or
even continue using) TADS 3/adv3Lite, although you will eventually find
them helpful when you want to achieve something beyond the basics.

### 2d. Using the Library Reference Manual

When you first gaze upon the [Adv3Lite Library Reference
Manual](libref/index.html) (LRM), it may appear to be an impenetrable
tangle, but in fact it's an extremely useful resource. To use it, you
need to be aware of the following basic ideas:

- The introductory page, which opens up when you click on the LRM in the
  Bookshelf page, contains a good description of how to use it.
- The links across the top change the contents of the index pane on the
  lower left. The most useful links may be "Classes" and "all symbols."
- Most Adv3Lite classes are derived from other classes, and inherit the
  properties and methods of those classes. For instance, in-game objects
  ultimately inherit from the Thing class. To see how the LRM works,
  choose the Classes pane (by clicking it in the top menu bar) and
  scroll down to the Door class in the lower left pane. Click on the
  word Door. You'll see a Superclass List, which shows which classes
  Door inherits from. A little lower down is an enormous list of
  Properties and Methods. All of these items are links. Clicking on any
  of them will take you to the place in the LRM where the property or
  method is shown.
- At the bottom of the page for a given class are the properties and
  methods that are unique to that class (and its subclasses). These
  descriptions are drawn directly from the comments in the Adv3Lite
  library source code.
- To the right of each property or method are two links: to the file in
  which the property or method is defined, and to the specific line on
  which it is defined. You will usually want to click on the line
  number, not on the filename.
- When you click on the line number, you'll be taken to the spot in the
  library source where that property or method is defined. By inspecting
  the code, you can often learn a great deal about how the property or
  method works.

## 3. Jumping Right In: A Sample Game

The sensible and logical thing to do at this point would be to start
reading one of the manuals suggested immediately above and, frankly,
that's what we recommend. But maybe you're thinking that having got as
far as installing adv3Lite and being shown how to compile a minimal
game, you'd like to actually try *doing* something with the system
before reading a whole lot of text. So, if you're the sort of person
that wants to jump right in, you might want to try entering and
compiling the sample game shown below. Few explanations are given —
that's what the manuals are for, after all — mainly just the source code
which you can either copy and paste into the Workbench editor (if you're
using Windows) or whatever other text editor/programming editor you're
using (if you're not on Windows) and then try compiling and running it.

If you do decide to type the code rather than copying and pasting, be
very careful to copy it *exactly*. (However, feel free to ignore the
comments in the code when retyping it. The comments are bracketed by the
symbols /\* and \*/, and are included here to give you a better idea
what you're seeing.) TADS 3 isn't too fussy about the amount of white
space you use or where you put line breaks, but it can be very fussy
about other things, and even the tiniest error can confuse it. In
particular:

- TADS 3 is *case sensitive*. That means that orb, ORB, Orb and oRb will
  all be taken to mean something different. You need to be absolutely
  sure to copy the precise case (upper or lower) of all the letters and
  words you type.
- Even the tiniest punctuation mark such as a bracket or a semicolon can
  be vital to how TADS 3 understands your source code. A single missing
  semicolon, for example, can confuse the compiler in ways that can be
  quite baffling to a new user. If you can't get your version to
  compile, check very closely for things like braces, commas, brackets
  and semicolons.

The sample game given below is given in three versions, each fuller and
more sophisticated than the last, so you can start from something very
simple and see how it might be built up into something more complex.
Don't worry if you don't understand too much of what's going on — at
this point you can hardly expect to, after all — just try copying and
compiling the code and then playing the resulting game to see what
happens. You may learn something from this approach, and you should at
least start to get some kind of feel for what writing a TADS 3 game
looks like. If you find at any stage that this approach is simply
confusing and frustrating, then give it up and go and start reading the
[Adv3Lite Tutorial](tutorial/index.htm) or [Learning TADS 3 With
Adv3Lite](learning/LearningT3Lite.pdf) instead. But if you feel you're
beginning to deduce how at least some of it works, then feel free to
experiment (but don't try anything too ambitious, you're probably not
ready for it yet).

I repeat, there is absolutely no need to carry out any of this exercise
at all; it's simply provided for people who are anxious to dive straight
in and try something practical before turning to the manuals. For some
people this approach may be helpful (as a kind of inductive learning
which will then help make the manuals make more sense); for many others
it probably won't help at all.

### Version 1

The plot of the game (such as it is) consists of the player character
entering a house, stealing the Orb of Ultimate Satisfaction, and then
escaping with it. We start with an absolutely basic bare bones
implementation.

    #charset "us-ascii"
    #include <tads.h>
    #include "advlite.h"

                            
                                /* The header, shown above, tells TADS to include some essential files. */
                            
                            versionInfo: GameID
                            IFID = '558c20af-6559-477a-9f98-b7b4274cd304'
                            name = 'The Best Burglar'
                            byline = 'by Eric Eve'
                            htmlByline = 'by <a href="mailto:eric.eve@dummy.com">
                            Eric Eve</a>'
                            version = '1'
                            authorEmail = 'Eric Eve <eric.eve@@dummy.com>'
                            desc = 'You are the world\'s best burglar faced with the greatest challenge
                            of your felonious career.'
                            htmlDesc = 'You are the world\'s best burglar faced with the greatest
                            challenge of your felonious career.'
                            ;

                            /* Notice that each object definition, including versionInfo, ends with a semicolon. */

                            gameMain: GameMainDef
                            /* The initial player character is an object called 'me', which will be defined shortly. */
                            initialPlayerChar = me
                            ;
                            
                                /* Objects in the game are created by giving the object a name that can be referred to in
                                your game code, then by stating what class the object is (in the case below, it's an
                                OutdoorRoom), and then giving it a name that will be displayed when the game is running. */

                            startRoom: Room 'Driveway'
                            "The great house stands before you to the north. "
                            north = hallway

                            roomAfterAction()
                            {
                            if(orb.isIn(me))
                            {
                            "Congratulations! You have just got away with the Orb of Ultimate
                            Satisfaction! ";
                            finishGameMsg(ftVictory, [finishOptionUndo]);
                            }
                            }
                            ;
                            
                                /* The plus sign on the first line of an object declaration tells TADS that this object
                                will be located inside of the previous object. */

                            + me: Thing 'you'
                            isFixed = true
                            person = 2  // change to 1 for a first-person game
                            contType = Carrier
                            ;
                            
                                /* Another room. Notice how the exits from the room are listed. The text in
                                double-quotes is the description of the room, and will be displayed when the player
                                enters the room or types 'look'. Notice also that text in TADS generally ends with
                                a space after the final period and before the closing quotation mark. */

                            hallway: Room 'Hallway'
                            "This hall is pretty bare, but there are exits to west and south. "
                            south = startRoom
                            west = study
                            ;

                            study: Room 'Study'
                            "This study is much as you would expect. A desk stands in the middle of the
                            room. The way out is to the east. "
                            east = hallway
                            ;
                            
                                /* The desk object has as single-quoted string in its declaration.  The first part,
                                before the semi-colon, defines the name, which is how the game will refer to it
                                when assembling text to show to the player. The second part creates
                                some additional vocabulary words that the player can use to refer to the desk.*/

                            + desk: Heavy, Platform 'desk; heavy wooden'
                            "It's a plain wooden desk; nothing fancy, just a horizontal surface on legs
                            but no drawers or anything like that. "
                            ;
                            
                                /* Notice that the orb is defined starting with TWO + signs. This will cause it to show
                                up on the desk.
                                */

                            ++ orb: Thing 'orb of ultimate satisfaction'
                            "It's -- well how can you describe such a thing? -- it's simply the most
                            valuable and desirable object in the known universe!"
                            ;
                        

The particular points to note here are the way rooms and other objects
are defined, and the way the + sign is used to locate some objects
inside others (such as rooms). Note also how the direction properties of
rooms (north, south, east, west) are used to provide the
interconnections between rooms. If you feel you can deduce how it's
done, you could try adding other basic objects and more rooms, with
connections between them, but if you don't feel confident about
experimenting, then by all means leave it and go on to the next version.

### Version 2

The first version wasn't much of a game. In the second we'll complicate
things a little by putting the orb in a locked safe to which the player
has to find the combination, and we'll provide the house with a locked
front door. While we're at it, we'll also define an object to represent
the house from the outside. We'll put the combination in a notebook in a
locked desk drawer, which means adding a drawer to the desk and
providing a key for it somewhere; we'll hide it in a vase in the hall.
We'll also make the hall look a bit more like it belongs in a big house
by adding a couple of fake exits that don't go anywhere but look as if
they do. And, of course, we need a key to the front door which for now
we'll just leave lying around in the drive. Finally, we'll provide a
proper introduction to the game and make it so that the game ends
(either in success or failure) when the player tries to return to the
road.

Once again, if you want to try this version out be very careful to copy
everything exactly, or it probably won't work. If you already have some
experienced with programming, especially in another IF authoring system,
you may be able to work out at least some of what's going on in the code
below, but if it totally baffles you it may be time to start reaching
for the manuals!

    #charset "us-ascii"
    #include <tads.h>
    #include "advlite.h"

                            versionInfo: GameID
                            IFID = '558c20af-6559-477a-9f98-b7b4274cd304'
                            name = 'The Best Burglar'
                            byline = 'by Eric Eve'
                            htmlByline = 'by <a href="mailto:eric.eve@dummy.com">
                            Eric Eve</a>'
                            version = '2'
                            authorEmail = 'Eric Eve <eric.eve@dummy.com>'
                            desc = 'You are the world\'s best burglar faced with the greatest challenge
                            of your felonious career.'
                            htmlDesc = 'You are the world\'s best burglar faced with the greatest
                            challenge of your felonious career.'
                            ;

                            gameMain: GameMainDef
                            /* the initial player character is 'me' */
                            initialPlayerChar = me

                            showIntro()
                            {
                            "<b>The Best Burglar</b>\nWell, you've got this far. Now it's just a
                            quick nip inside the house and out again carrying the Orb of Ultimate
                            Satisfaction, an object that no burglar has ever managed to steal
                            before. If you can pull it off you're sure to win the Burglar of the
                            Year Award, putting you at the pinnacle of your profession.\b";
                            }
                            ;
                            
                                /* The asExit line in the room below will cause TADS to interpet the command 'in' exactly
                                as if the player had typed 'north'. */

                            startRoom: Room 'Driveway'
                            "Here you are in the drive of Number 305 Erehwon Avenue, with the great
                            house you've come to burgle standing just before you to the north. The
                            drive back to the road where you left your getaway vehicle runs off
                            to the southwest. "
                            north = frontDoor
                            in asExit(north)
                            southwest = drive
                            ;
                            
                                /*
                                *   You can use the Player class to define the player character to save typing the
                                *   necessary properties on Thing, although here we add a name property and a description
                                *   to give a meaningful response to an EXAMINE ME command. If you use the Player class
                                *   to define the initial player character, you don't actually need to define the
                                *   initialPlayerChar property on gameMain, since the Player object will register itself,
                                *   but you still need to define the gameMain object and defining its initialPlayerChar
                                *   property may feel clearer.
                                */

                            + me: Player 'you'
                            "You're Alexis Lightfinger, burglar extraordinaire, the most
                            professional thief in the known universe; but you're on a job now, so
                            you don't have time for the narcissistic indulgence of admiring your own
                            appearance. You're far too professional not to have come fully prepared,
                            so there's no practical need to look yourself over again. "
                            ;

                            ++ Container 'swag bag; large white'
                            "It's a large white bag with <q>SWAG</q> printed on it in very large
                            letters. Everyone knows that no real burglar would ever carry such a thing,
                            so by carrying it you know no one will take you for a real burglar. Cunning,
                            eh? "
                            ;
                            
                                /*
                                *   The frontDoor object is in the same location as me and the brassKey. TADS
                                *   understands that doors are usually scenery, so no special effort is needed
                                *   to prevent the game from reporting, "You can see a front door here."
                                */

                            + frontDoor: Door 'front door'
                            lockability = lockableWithKey
                            otherSide = hallDoor
                            isLocked = true
                            ;

                            + brassKey: Key 'small brass key'
                            "It's an ordinary enough small brass key. "
                            initSpecialDesc = "A small brass key lies on the ground near the door. "

                            actualLockList = [frontDoor, hallDoor]
                            ;
                            
                                /*
                                *   The next object is an anonymous object. That is, it has no in-code name of
                                *   its own, because the game code never needs to refer to it. The arrow
                                *   pointing to frontDoor tells TADS where to send the player if he should type
                                *   'enter the house'. As you can see from the description, this object is the
                                *   exterior of the house.
                                */

                            + Enterable 'house; large tudor; mansion buildings[pl]'
                            "It's a large Tudor house with mullioned windows. "

                            connector = frontDoor
                            ;

                            + drive: PathPassage 'drive;; path'
                            "The drive leading back to the road runs off to the southwest. "

                            noteTraversal(traveler)
                            {
                            "You retrace your steps back to the road, where your trusty unmarked
                            burglarmobile is still parked, ready for your quick getaway. ";

                            if(orb.isIn(me))
                            {
                            "Congratulations! You have got away with the Orb of Ultimate
                            Satisfaction, a feat never before performed. As you slip the orb
                            onto the back seat of your car and climb into the driver's seat
                            you tell yourself that you're now absolutely certain to win
                            the Burglar of the Year Award!\b";

                            finishGameMsg(ftVictory, [finishOptionUndo]);
                            }
                            else
                            {
                            "It's a shame you didn't manage to steal the orb, though.
                            Without it you'll never win the Burglar of the Year Award
                            now.\b";

                            finishGameMsg(ftFailure, [finishOptionUndo]);
                            }

                            }
                            ;



                            hallway: Room 'Hallway'
                            "This hall is or grand proportions but pretty bare. The front door lies to
                            the south and other exits lead east, north and west. "

                            south = hallDoor
                            out asExit(south)
                            west = study
                            north() { "You're pretty sure that only leads to the kitchen,
                            and you haven't come here to cook a meal. "; }

                            east() { "You <<one of>>walk through the doorway and find yourself
                            in<<or>>return to<<stopping>> the living room where you take <<one of>>
                            a <<or>>another<<stopping>> quick look around, but <<one of>><<or>> once
                            again<<stopping>> failing to find anything of interest you quickly
                            return to the hall. "; }
                            ;

                            + hallDoor: Door 'front door'
                            lockability = lockableWithKey
                            otherSide = frontDoor
                            isLocked = true
                            ;

                            + table: Surface 'small table; wooden mahogany side; legs'
                            "It's a small mahogany table standing on four thin legs. "
                            initSpecialDesc = "A small table rests by the east wall. "
                            ;

                            ++ vase: Container 'vase; cheap china floral; pattern'
                            "It's only a cheap thing, made of china but painted in a tasteless floral
                            pattern using far too many primary colours. "

                            hiddenIn = [silverKey]
                            ;
                            
                                /*
                                *   Since the silver key is in the hiddenIn list of the vase, it will be found
                                *   when the player looks in the vase.
                            */
                            silverKey: Key 'small silver key'
                            actualLockList = [drawer]
                            ;

                            study: Room 'Study'
                            "This study is much as you would expect: somewhat spartan. A desk stands in
                            the middle of the room with a chair placed just behind it. The way out is to
                            the east. "
                            east = hallway
                            out asExit(east)
                            ;

                            + desk: Heavy, Platform 'desk; plain wooden'
                            "It's a plain wooden desk with a single drawer. "

                            remapIn = drawer
                            ;

                            ++ drawer: Component, KeyedContainer 'drawer; (desk)'
                            "It's an ordinary desk drawer with a small silver lock. "
                            isLocked = true
                            ;

                            
                                /*
                                *   The notebook object needs some special code for the command 'open
                                *   notebook'. The dobjFor macro creates some code for the Open action, and the
                                *   asDobjFor(Read) code causes 'open notebook' to have the same result as
                                *   'read notebook.
                            */

                            +++ notebook: Thing 'small red notebook; bright; book cover pages'
                            "It's a small notebook with a bright red cover. "

                            readDesc = "You open the notebook and flick through its pages. The only
                            thing you find of any interest is a page with 1589 scrawled across it.
                            After satisfying yourself that the notebook contains nothing else of
                            any potential relevance you snap it shut again. "

                            dobjFor(Open) asDobjFor(Read)
                            cannotCloseMsg = 'It\'s already closed. '
                            ;

                            + Immovable, Platform 'chair; red office swivel'
                            "It's a typical office swivel chair, covered in red fabric. "
                            cannotTakeMsg = 'You see no reason to burden yourself with such a useless
                            object; that would be quite unprofessional. '
                            canLieOnMe = nil
                            ;

                            + safe: Fixture,  OpenableContainer
                            'sturdy steel safe'
                            "It's a sturdy steel safe with a single dial on its door. "
                            specialDesc = "A safe is built into one wall. "
                            cannotTakeMsg = 'It\'s firmly built into the wall; you can't budge it. '
                            lockability = indirectLockable
                            ;

                            ++ orb: Thing 'orb of ultimate satisfaction; battered dull metal; sphere ball'
                            "It doesn't look much be honest, just a battered sphere made of some dull
                            metal, but you've been told it's the most valuable and desirable object
                            in the known universe! "

                            aName = (theName)
                            ;
                            
                                /*
                                *   Notice how the double angle brackets are used to let the description of the
                                *   safe refer to the properties of the object. This is an extremely common and
                                *   useful technique in TADS.
                                */

                            + safeDial: NumberedDial, Fixture 'dial'
                            "The dial can be turned to any number between <<minSetting>> and
                            <<maxSetting>>. It's currently at <<curSetting>>. "

                            minSetting = 0
                            maxSetting = 99
                            curSetting = '35'

                            num1 = 0
                            num2 = 0
                            correctCombination = 1589

                            makeSetting(val)
                            {
                            inherited(val);
                            num2 = num1;
                            num1 = toInteger(val);
                            if(100 * num2 + num1 == correctCombination)
                            {
                            "You hear a slight <i>click</i> come from the safe door. ";
                            safe.makeLocked(nil);
                            }
                            else if(!safe.isOpen)
                            safe.makeLocked(true);
                            }

                            cannotTakeMsg = 'It\'s firmly attached to the safe. '
                            ;
                        

There are too many new features to discuss in detail here, but one or
two of them are worth briefly pointing out. Note how the front door to
the house is implemented as *two* objects, each representing one side of
the door, and how they are linked by having each side point to the other
via their otherSide properties. Note also how the north and south
properties of the driveway and the hall now point to one or other side
of the door. You may also have noticed how objects can be defined as
belonging to more than one class (e.g. the safeDial immediately above is
both a NumberedDial so we can turn it to a particular number and a
Fixture so we can't pick it up and walk away with it). You'll probably
have worked out that a Surface is something you can put things on and a
Container is something you can put things inside. A Platform is
something you can stand, sit or lie on as well (we make the desk a
Platform because it's presumably big enough and sturdy enough to get
on).

At this point you may want to experiment with adding or changing a few
things to see how they work, or you may think you've had enough of
copying code you don't understand (in which case it's probably time to
head for the manuals) or you may want to go on and try out the third and
final version of "The Best Burglar".

### Version 3

We'll make the third and final version of “The Best Burglar” just a
*little* more challenging by hiding the front door key under a
flowerpot, hiding the safe behind a picture, and making the clue to the
combination in the notebook a bit more cryptic. We'll also make the Orb
of Ulimate Satisfaction a tad more interesting by making it do something
(albeit not that much) when it's rubbed, which means we'll also need to
define a new RUB verb. We'll add a few decoration objects to field
commands directed at things mentioned in room descriptions and the like,
and we'll tidy up a couple of things, by, for example, defining the bulk
and bulk capacity of various objects so the player can't put something
obviously bigger inside something obviously smaller, and, for example,
by preventing the player picking up the hall table when there's
something still on it. Finally, we'll add some scoring and hints to the
game.

    #charset "us-ascii"
    #include <tads.h>
    #include "advlite.h"

                            versionInfo: GameID
                            IFID = '558c20af-6559-477a-9f98-b7b4274cd304'
                            name = 'The Best Burglar'
                            byline = 'by Eric Eve'
                            htmlByline = 'by <a href="mailto:eric.eve@dummy.com">
                            Eric Eve</a>'
                            version = '3'
                            authorEmail = 'Eric Eve <eric.eve@dummy.com>'
                            desc = 'You are the world\'s best burglar faced with the greatest challenge
                            of your felonious career.'
                            htmlDesc = 'You are the world\'s best burglar faced with the greatest
                            challenge of your felonious career.'
                            ;

                            gameMain: GameMainDef
                            /* the initial player character is 'me' */
                            initialPlayerChar = me

                            showIntro()
                            {
                            "<b>The Best Burglar</b>\nWell, you've got this far. Now it's just a
                            quick nip inside the house and out again carrying the Orb of Ultimate
                            Satisfaction, an object that no burglar has ever managed to steal
                            before. If you can pull it off you're sure to win the Burglar of the
                            Year Award, putting you at the pinnacle of your profession.\b";
                            }

                            showGoodbye()
                            {
                            "Thanks for playing! ";
                            }
                            ;

                            startRoom: Room 'Driveway'
                            "<<one of>>Here you are in the drive of Number 305 Erehwon Avenue, with the
                            great house you've come to burgle standing just before you to the north. The
                            <<or>>The large red-brick Tudor house stands immediately to the north of
                            this end of the driveway, while the <<stopping>> drive back to the road
                            where you left your getaway vehicle runs off to the southwest. "

                            north = frontDoor
                            in asExit(north)
                            southwest = drive
                            ;
                            
                                /*
                                *   The player character object. This doesn't have to be called me, but me is a
                                *   convenient name. If you change it to something else, rememember to change
                                *   gameMain.initialPlayerChar accordingly.
                                */

                            + me: Thing 'you'
                            "You're Alexis Lightfinger, burglar extraordinaire, the most
                            professional thief in the known universe; but you're on a job now, so
                            you don't have time for the narcissistic indulgence of admiring your own
                            appearance. You're far too professional not to have come fully prepared,
                            so there's no practical need to look yourself over again. "

                            isFixed = true
                            person = 2  // change to 1 for a first-person game
                            contType = Carrier
                            ;

                            ++ Container 'swag bag; large white'
                            "It's a large white bag with <q>SWAG</q> printed on it in very large
                            letters. Everyone knows that no real burglar would ever carry such a thing,
                            so by carrying it you know no one will take you for a real burglar. Cunning,
                            eh? "
                            ;
                            
                                /*
                                *   The frontDoor object is in the same location as me and the brassKey. TADS
                                *   understands that doors are usually scenery, so no special effort is needed
                                *   to prevent the game from reporting, "You can see a front door here."
                                */

                            + frontDoor: Door 'front door; solid oak'
                            "The lintel above the front door is carved with the date 1589, presumably
                            the date the house was built. The door itself is made of solid oak. "

                            lockability = lockableWithKey
                            otherSide = hallDoor
                            isLocked = true

                            makeOpen(stat)
                            {
                            inherited(stat);
                            if(stat)
                            achievement.awardPointsOnce();
                            }

                            achievement: Achievement { +10 "opening the front door" }
                            ;



                            + flowerPot: Container 'flower pot; terracotta small flower'
                            "It's a perfectly ordinary small terracota pot, though it looks like no
                            one's got round to putting a plant in it yet. "

                            bulkCapacity = 3
                            bulk = 3

                            initSpecialDesc = "A small flower pot rests on the ground not far from the
                            front door. "

                            hiddenUnder = [brassKey]
                            ;


                            + Enterable 'house; large tudor; mansion buildings[pl]'
                            "It's a large red-brick Tudor house with mullioned windows, climbing
                            creepers and the date 1589 carved over the door. "

                            connector = frontDoor
                            ;

                            ++ Component 'lintel; (door) carved'
                            "Its most noteworthy feature is the date 1589 carved into it. "
                            ;

                            + Decoration 'windows; mullioned;; them'
                            "They're architecturally attractive, no doubt, but not especially helpful to
                            burglars. "

                            notImportantMsg = 'It\'s a matter of professional pride with you never to
                            mess with windows. '
                            ;

                            + Decoration 'creepers; green climbing; creeper ivy; them it'
                            "The front of the house is festooned with green creepers -- ivy, perhaps,
                            but botany was never your strong point since in the main plants aren't
                            worth burgling. "

                            notImportantMsg = 'The creepers can\'t help you burgle the house -- they\'re
                            certainly not strong enough to climb and they\'re certainly not worth
                            stealing -- so you may as well leave them alone. '
                            ;


                            + drive: PathPassage 'drive;;path avenue'
                            "The drive leading back to the road runs off through a belt of trees to the
                            southwest. "

                            travelDesc
                            {
                            "You retrace your steps back to the road, where your trusty unmarked
                            burglarmobile is still parked, ready for your quick getaway. ";

                            if(orb.isIn(me))
                            {
                            "Congratulations! You have got away with the Orb of Ultimate
                            Satisfaction, a feat never before performed. As you slip the orb
                            onto the back seat of your car and climb into the driver's seat
                            you tell yourself that you're now absolutely certain to win
                            the Burglar of the Year Award!\b";

                            achievement.awardPointsOnce();

                            finishGameMsg(ftVictory, [finishOptionUndo,
                            finishOptionFullScore]);
                            }
                            else
                            {
                            "It's a shame you didn't manage to steal the orb, though.
                            Without it you'll never win the Burglar of the Year Award
                            now.\b";

                            finishGameMsg(ftFailure, [finishOptionUndo]);
                            }

                            }

                            okayRubMsg = 'What -- all of it? That may take a while! '
                            achievement: Achievement { +10 "getting away with the orb" }
                            ;

                            + Decoration 'trees; of[prep]; belt; them'
                            "The trees are in full leaf, which is good, because they hide what you're
                            doing from the road. "

                            notImportantMsg = 'The trees are doing a good job of hiding you from the
                            road, so you may as well leave them alone. It\'s not as if they\'re
                            something you could steal, after all. '
                            ;

                            brassKey: Key 'small brass key'
                            "It's an ordinary enough small brass key. "

                            actualLockList = [frontDoor, hallDoor]
                            ;

                            hallway: Room 'Hallway'
                            "This hall is or grand proportions but pretty bare. The front door lies to
                            the south and other exits lead east, north and west. "

                            south = hallDoor
                            out asExit(south)
                            west = study
                            north() { "You're pretty sure that only leads to the kitchen,
                            and you haven't come here to cook a meal. "; }

                            east() { "You <<one of>>walk through the doorway and find yourself
                            in<<or>>return to<<stopping>> the living room where you take <<one of>>
                            a <<or>>another<<stopping>> quick look around, but <<one of>><<or>> once
                            again<<stopping>> failing to find anything of interest you quickly
                            return to the hall. "; }
                            ;

                            + hallDoor: Door 'front door'
                            lockability = lockableWithKey
                            otherSide = frontDoor
                            isLocked = true
                            ;

                            + table: Surface 'small table; wooden mahogany side; legs'
                            "It's a small mahogany table standing on four thin legs. "
                            initSpecialDesc = "A small table rests by the east wall. "

                            bulk = 5

                            dobjFor(Take)
                            {
                            check()
                            {
                            if(contents.length > 0)
                            "It's probably not a very good idea to try picking up the table
                            while <<contents[1].theNameIs>> still on it. ";
                            }
                            }
                            ;


                            ++ vase: Container 'vase; cheap china floral; pattern'
                            "It's only a cheap thing, made of china but painted in a tasteless floral
                            pattern using far too many primary colours. "

                            hiddenIn = [silverKey]
                            ;
                            
                                /*
                                *   Since the silver key is in the hiddenIn list of the vase, it will be found
                                *   when the player looks in the vase.
                                */
                            silverKey: Key 'small silver key'
                            actualLockList = [drawer]
                            ;


                            study: Room 'Study'
                            "This study is much as you would expect: somewhat spartan. A desk stands in
                            the middle of the room with a chair placed just behind it. A <<if
                            picture.moved>>safe is built into <<else>> rather bland painting hangs on
                            <<end>> the west wall. The way out is to the east. "
                            east = hallway
                            out asExit(east)
                            ;

                            + desk: Heavy, Platform 'desk; plain wooden'
                            "It's a plain wooden desk with a single drawer. "

                            remapIn = drawer
                            ;

                            ++ drawer: Component, KeyedContainer 'drawer; (desk)'
                            "It's an ordinary desk drawer with a small silver lock. "
                            isLocked = true
                            ;

                            +++ notebook: Thing 'small red notebook; bright; book cover pages'
                            "It's a small notebook with a bright red cover. "

                            readDesc = "You open the notebook and flick through its pages. The only
                            thing you find of any interest is a page with <q>SAFE DATE</q> scrawled
                            across it. After satisfying yourself that the notebook contains nothing
                            else of any potential relevance you snap it shut again. <.reveal
                            safe-date>"

                            dobjFor(Open) asDobjFor(Read)
                            dobjFor(LookIn) asDobjFor(Read)

                            dobjFor(Read)
                            {
                            action()
                            {
                            inherited;
                            achievement.awardPointsOnce();
                            }
                            }

                            cannotCloseMsg = 'It\'s already closed. '
                            achievement: Achievement { +5 "reading the notebook" }
                            ;

                            + Immovable, Platform 'chair; red office swivel'
                            "It's a typical office swivel chair, covered in red fabric. "
                            cannotTakeMsg = 'You see no reason to burden yourself with such a useless
                            object; that would be quite unprofessional. '
                            canLieOnMe = nil
                            ;

                            + picture: Thing 'picture; rather bland; painting landscape'
                            "It's a landscape, pleasantly executed enough, but of no great distinction
                            and definitely not worth the bother of stealing. "

                            initSpecialDesc = "A rather bland painting hangs on the west wall. "
                            isListed = (moved)

                            bulk = 8

                            hiddenBehind = [safe]
                            ;

                            safe: Fixture 'safe; sturdy steel'
                            "It's a sturdy steel safe with a single dial on its door. "
                            specialDesc = "A safe is built into one wall. "
                            cannotTakeMsg = 'It\'s firmly built into the wall; you can\'t budge it. '

                            remapIn: SubComponent, OpenableContainer
                            {
                            lockability = indirectLockable
                            isLocked = true
                            }

                            achievement: Achievement { +5 "finding the safe" }

                            moveInto(loc)
                            {
                            inherited(loc);
                            achievement.awardPointsOnce();
                            }
                            ;

                            + orb: Thing 'orb of ultimate satisfaction; battered dull metal; sphere ball'
                            "It doesn't look much be honest, just a battered sphere made of some dull
                            metal, but you've been told it's the most valuable and desirable object
                            in the known universe! "

                            aName = (theName)
                            
                                /*
                                *   Note how we start the orb off inside the remapIn SubComponent of the
                                *   safe.
                                */
                            subLocation = &remapIn

                            okayRubMsg = 'As {i} rub{s/?ed} {the dobj} a shimmering djiin suddenly
                            appears in the air before you!\b
                            <q>Hello, you have reached the automated holographic answering service
                            of Jeannie the Genie,</q> she announces. <q>I\'m sorry I\'m not
                            available to respond to your rub in person right now, but my hours of
                            activity have been heavily curtailed by the European Working Time
                            Directive. Before making a wish, please make sure that you have
                            conducted a full risk assessment in line with the latest Health and
                            Safety Guidelines. Also, please note that before any wish can be granted
                            you must sign a Form P45/PDQ/LOL indemnifying this wish-granting agency
                            against any consequential loss or damage arising from the fulfilment of
                            your desires. Thank you for rubbing. Have a nice day!</q>\b
                            Her message complete, the holographic djiin fades away into
                            non-existence. '

                            moveInto(dest)
                            {
                            inherited(dest);
                            if(dest.isOrIsIn(me))
                            achievement.awardPointsOnce();
                            }

                            achievement: Achievement { +10 "taking the orb" }
                            ;
                            
                                /*
                                *   We make the safeDoor a ContainerDoor, which means that it is open or closed
                                *   according to whether its location (the safe) is open or closed, and actions
                                *   applied to the door such as OPEN and CLOSE are actually applied to the safe.
                                */
                            + safeDoor: ContainerDoor 'safe door'
                            "It has a circular dial attached to its centre. "
                            ;

                            
                                /*
                                *   Notice how the double angle brackets are used to let the description of the
                                *   safe refer to the properties of the object. This is an extremely common and
                                *   useful technique in TADS.
                                */

                            ++ safeDial: NumberedDial, Fixture 'dial'
                            "The dial can be turned to any number between <<minSetting>> and
                            <<maxSetting>>. It's currently at <<curSetting>>. "

                            minSetting = 0
                            maxSetting = 99
                            curSetting = '35'

                            num1 = 0
                            num2 = 0
                            correctCombination = 1589

                            makeSetting(val)
                            {
                            inherited(val);
                            num2 = num1;
                            num1 = toInteger(val);
                            if(100 * num2 + num1 == correctCombination)
                            {
                            "You hear a slight click come from the safe door. ";
                            safe.remapIn.makeLocked(nil);
                            }
                            else if(!safe.isOpen)
                            safe.remapIn.makeLocked(true);
                            }

                            cannotTakeMsg = 'It\'s firmly attached to the safe. '
                            ;



                            //------------------------------------------------------------------------------
                            
                                /* DEFINE A NEW VERB */

                            DefineTAction(Rub)
                            ;

                            VerbRule(Rub)
                            'rub' multiDobj
                            : VerbProduction
                            action = Rub
                            verbPhrase = 'rub/rubbing (what)'
                            missinqQ = 'what do you want to rub'
                            ;
                            
                                /*
                                *   When creating a new verb, you'll want to modify the Thing class so as to
                                *   provide default handling for the command. The defaults specified here will
                                *   be used except on objects for which you define explicit handling of the
                                *   command.
                                */

                            modify Thing
                            dobjFor(Rub)
                            {
                            preCond = [touchObj]
                            action() { say(okayRubMsg); }
                            }

                            okayRubMsg = '{I} rub{s/?ed} {the dobj} but not much happens as a
                            result. '

                            shouldNotBreakMsg = 'Only amateurs go round breaking things unnecessarily. '
                            ;

                            //------------------------------------------------------------------------------
                            
                                /* HINTS */

                            TopHintMenu;

                            + Goal -> (frontDoor.achievement)
                            'How do I get into the house?'
                            [
                            'Well, the windows don\'t seem a good way in. ',
                            'So perhaps you\'d better try the front door. ',
                            'Could someone have left a key around somewhere? ',
                            'Is there anything lying around where someone could have hidden a key? ',
                            'What about that flowerpot? ',
                            'Try looking under the flowerpot. '
                            ]

                            goalState = OpenGoal
                            ;
                            
                                /* The closeWhenSeen property of the following Goal object is an example of how to
                                make your hint menu respond dynamically to the player's current situation. */

                            + Goal 'Where can I find the orb? '
                            [
                            'Something like that is bound to be kept safe. ',
                            'So it\'s probably inside the house. '
                            ]

                            goalState = OpenGoal
                            closeWhenSeen = hallway
                            ;

                            + Goal 'Where can I find the orb?'
                            [
                            'It\'s sure to be kept somewhere safe. ',
                            'You\'d better hunt around. ',
                            'Somewhere in the study seems the most likely place. ',
                            deskHint,
                            'But it should be safely locked in a safe ',
                            'Where might someone hide a safe in this study? ',
                            'What could be behind that picture on the wall? ',
                            'Try looking behind the picture (or simply taking the picture). '
                            ]

                            openWhenSeen = hallway
                            closeWhenSeen = orb
                            ;

                            ++ deskHint: Hint 'Have you tried looking in the desk drawer? '
                            [deskGoal]
                            ;

                            + deskGoal: Goal 'How do I get the desk drawer open?'
                            [
                            'Have you examined the drawer? ',
                            'What might you need to unlock it? ',
                            'Where might you find such a thing? ',
                            'What have you seen that a small key might be hidden in? ',
                            'How carefully have you searched the hall? ',
                            'What is (or was) on the hall table? ',
                            'What might that vase be for? ',
                            'Try looking in the vase. '
                            ]
                            closeWhenSeen = notebook
                            ;

                            + Goal 'How do I get the safe open?'
                            [
                            'How carefully have you examined the safe? ',
                            'Where might someone leave a clue to the combination? ',
                            deskHint,
                            'Make sure you read the notebook. ',
                            'Once you\'ve found the combination you need to use the dial. ',
                            'If the combination is a number larger than 99 you\'ll need to enter it
                            in stages. ',
                            'For example, if the combination were 1234 you\'d first need to turn the
                            dial to 12 and then turn it to 34. '
                            ]

                            openWhenSeen = safe
                            closeWhenAchieved = (safe.remapIn.achievement)
                            ;

                            + Goal 'What does the clue in the notebook mean?'
                            [
                            'Well, <q>SAFE</q> might refer to something you want to open. ',
                            'Have you seen a date round here? ',
                            'When was this house built? ',
                            'Where might you find the year in which this house was built? ',
                            'How carefully have you looked at the front of the house? ',
                            'Did you examine the door? '
                            ]

                            openWhenRevealed = 'safe-date'
                            closeWhenAchieved = (safe.remapIn.achievement)
                            ;


                            + Goal 'What do I do with the orb now I\'ve got it?'
                            [
                            'Well, you could try rubbing it. ',
                            'But the main thing to do now is to escape with it. '
                            ]
                            openWhenSeen = orb
                            ;
                        

Doubtless there a great many more things that could be done to improve
this game, but it has now served its purpose.

Once again, there are far too many features here to discuss in a Quick
Start Guide. One thing in particular to note is the use of the
`SubComponent` class. We use it for the inside of the safe, because we
have now made the safe door a Component of the safe and the combination
dial a Component of the safe door. If we had left the safe as an
OpenableContainer (as in version 2), the safe door and the combination
dial would have been locked inside the safe along with the orb, and the
safe would have been impossible to open (a mistake it's very easy to
make, so this is worth noting). Another thing worth noting is the use of
`remapIn` to redirect certain actions that the player might reasonably
try on the desk to its drawer. Finally it's worth pointing out that
there's more than one way we could have implemented many of the things
shown above.

There are plenty of other feature of adv3Lite that haven't been
introduced yet. In particular this example doesn't even begin to touch
on the creation of NPCs (other characters in your game — the fleeting
appearance of Jeannie the Genie doesn't really count). But the three
versions of the game shown above should have illustrated quite a few of
the most common features of adv3Lite and TADS 3 used in developing
adv3Lite games, and depending on your background and inclinations you
may have learned something by studying the sample code and trying it
out. If you feel confident enough to experiment a little more on your
own, by all means do so, but at this stage it's getting pretty near the
point when you will need to move on to the [Adv3Lite
Tutorial](tutorial/index.htm) or [Learning TADS 3 With
Adv3Lite](learning/LearningT3Lite.pdf).

*Eric Eve — October 2022*
