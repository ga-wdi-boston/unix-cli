A couple of years ago I bumped into an old schoolmate of mine,
Morty. Now Morty was kind of a hardware geek. I mean stuff in
hardware stores like nails, saws, electrical fixtures, ya know.

We'll Morty had an idea awhile ago, now that he a was a fully grown
geek and had saved up a bunch of money from working in the nail
factory. He wentinto the hardware store business.

And Morty knew I had had been working with "the computers" and thought
I might know something about "the programs" and "the internets". See,
Morty kinda lived in 1945 and only begrudgingly picked up these highly
technical terms like "the computers" and "the internets".

Even though he wasn't happy about it he read in a a highly popular
industry journal that hardware store proprietors where now expected to
use "the internets" and "the computers".

So, upon seeing me he dove right into a campaign to play upon the very
sliver of a relationship we had decades ago. He was trying to get me
to do some free work for him. The fool.

I told him I could help him out, but he wasn't gonna get much for the
price. Of course, he didn't hear that part and just launched into a
tirade about how has structured his store, price his items organized
all the bits and hardware bobs.

Now I'm kind of like, Whoa slow done Morty let me get the laptop out
and we'll sit over on this bench over here. Hey, Morty you got about
thirty minutes of a highly paid software developer's time for nothing
so let's go through this in a highly ordered and structured way, you
pain in the butt you.

BTW, I never really liked Morty after that time he shook my hand with
a fully charged capacitor and shocked the hell out of me. I should
really screw this little project up royally, huh? Payback.

Ok Mort. What you're getting for nothing is a project that contains a
set of important files organized in a way that, hopefully, will make
sense for your business. You'll be able to easily locate, organize,
capture and generally manage the information that relates to your
business.

No web applications, I charge money to people I sometimes like for
that service. And you aren't paying me and, ahh, you know what I think
about you after that shocking experience all those years ago.

First Morty, no,no stop talking, wait, wait the clock is ticking
here. I'm going to ask you a set of targeted questions about you
business **domain**, the hardware stores, and you're going to answer
in the breif way.

What am I doing this for?

Now let's get onto the job of helping Mort out.

First Morty, what are the departments in your store?

He tells me "Lawn and Garden", Plumbing, Electrical, Tools and
Hardware.

And what kinds of products are in each department?

Lawn and Garden - Patio furniture, Hoses, Rakes, Shovels.
Plumbing - Toilets, Sinks, Tube and Showers, Pipes, Fittings, Solder
Electrical - Fuses, Lighting, Batteries, Switches, Wiring.
Tools - Hand Tools, Power Tools, Wet/Dry Vacuums, Work Benches.
Hardware - Door and Window, Fasteners.

Ok, Morty you're gonna the work here because I'm outa here in
about 25 minutes and I don't want to see your face for another 35
years, haha. No really, I'm not kidding.

* Let's open up the terminal to get a command line interface(CLI) we
  can work in.

** Clicking in the hour glass in the upper-right side of window, in
the menu up there. Then type 'terminal' and hit return.

** Alternatively, you can type:
CMD-Space
      To bring up Spotlight search.
Enter "terminal" with no quotes  and hit return.
      To start the terminal program.

Good, now Morty this is where real developers do a lot, I mean a lot
of their work. And you might like this because it's a little closer to
the time warp your living in. It's been around since probably the
sixties, I've been using it since 1976 myself.

* Let's see where in the computer's file system we are?

(Note: the command to type will be preceded by the '$' character
And the command's output, if shown, will be preceded by the '=>'
characters)

$ pwd
=> /Users/tdyer

This will show you what the "present working directory" is. You might
of heard directories called folders. It what one uses to organize
files in the computer's file system.

Oh, look the "present working directory" is my home, or default,
directory. We're seeing the "absolute path" of my home directory.

*** Absolute path
An absolute path shows one the location of the files and directories
with the system's file system. Absolute paths:
- Always start with a leading slash, '/'
- Are relative to the root directory of the file system.

*** Root directory
Is the top level directory in the tree structure of the filesystem.

* Open up the Finder and go to the root directory of your filesystem.

* Find you're home directory in the filesystem. Hint: use the absolute
  file path returned from the pwd above to find this.

* Lets start a project for your store Morty by organizing all your
project files into it's own directory.

$ mkdir MortStore

** This will make a directory named "MortStore" in my home
   directory. See mkdir is "make directory", amazing!

* Lets change into the "root", or top directory of your project. Not
  the root of the filesystem, the root of this new project.

$ cd MortStore

** This will "change directory" into the MortStore. This will hold all
   the files and such for your project.

* Let's see what the contents of this directory are.

$ ls

** This will "list" all the files and subdirectories in the MortStore
   directory. None yet.

* Let's create a README file that will be a high level description of
  this project.

$ touch README

** This will create an empty file named README if one doesn't already
   exist.

* Let's look all files our project, only the empty README right now.

$ ls
=> README
$ ls -l
=> -rw-r--r--  1 tdyer  staff  0 Sep 25 01:55 README

** 'ls -l' will list the contents of the current directory in "long"
   form. It show the permissions to the files and directories,
   -rw-r--r--. Followed by number of links, 1, owner name, tdyer,
   group name, staff, number of bytes in file, 0, last modified date
   and time.

(From here on out we are going to use BOTH the command line and
Sublime to view the project and possible modify the project).

* Look at and modify our project using the Sublime Text Editor.
$ subl .

** This will run the Sublime Text Editor for you project. The dot,
   '.', after subl represents the current directory we're working
   in. So we're opening Sublime in the current directory which will
   show us Morty's project.

*** 'Dot' directory
    The dot, '.' directory is a reference to the current directory
    your working in.

* Add the below to the README file and save it.

Morty's Hardware
Lawn and Garden - Patio furniture, Hoses, Rakes, Shovels.
Plumbing - Toilets, Sinks, Tube and Showers, Pipes, Fittings, Solder
Electrical - Fuses, Lighting, Batteries, Switches, Wiring.
Tools - Hand Tools, Power Tools, Wet/Dry Vacuums, Work Benches.
Hardware - Door and Window, Fasteners.

* Go back to the Terminal and show the contents of the root directory.
$ pwd
$ ls
$ ls -l
=> -rw-r--r--  1 tdyer  staff  306 Sep 25 02:18 README
$ cat README

** cat will print the contents of the file README. This is just to
   check that you modified the right file.

* Create subdirectories for each department.

$ mkdir LawnGarden
$ mkdir Plumbing
$ mkdir Electrical
$ mkdir Tools
$ mkdir Hardware

* View all files in your project

$ ls -lR

** -R will recurse through all the subdirectories and run ls -l to show
    all the files and subdirectories of the current directory.

* Determine that the view your seeing from ls -lR EXACTLY matches with
the view of your project your seeing in Sublime.

* In Sublime create a file that will track the inventory for each department.

The files will be named inventory.txt and there contents will be a
comma seperated file (CSV).

** In LawnGarden/inventory.csv

Item,ProdNum,Quantity,Price,Sold Per Month
Shovel, 1, 11,74.33,13
Rake,2,5,35.99,0.5
Hose,3,19,16.99,3

** In Plumbing/inventory.csv:
Item,ProdNum,Quantity,Price,Sold Per Month
Toilet,4,3,249.99,1
Solder,5,88,5.99,33
Sinks,6,5,299.99,.2

** In Electrical/inventory.csv:
Item,ProdNum,Quantity,Price,Sold Per Month
Fuses,7,1024,1.99,640
Batteries,8,100,4.99,204
Switchs,9,29,14.50,18

** In Tools/inventory.csv:
Item,ProdNum,Quantity,Price,Sold Per Month
Hand Saw,10,9,77.99,2
Drill,11,67,34.99,15
Wet Vac,12,2,114.50,0.1


* Now create a file in each directory that will capture the current
  employees working in each department.

** In LawnGarden/staff.csv:

Name,Phone,Email,Role
Jack Sprat,978-251-2384,jack@example.com,manager
Moe Brown,617-589-8977,moeb@example.com, associate

** In Plubming/staff.csv:

Name,Phone,Email,Role
Brian Behan,978-668-2344,brianb@example.com,manager
Richy Havens,617-812-7312,rhavens@example.com, associate

** In Electrical/staff.csv:

Name,Phone,Email,Role
Joy Gillis,978-238-9894,joyg@example.com,manager
Laura Havens,617-763-5542,rhavens@example.com, associate

** In staff.csv:
Name,Phone,Email,Role
Tom Smith,888-989-777,ts@example.com, associate
Meg Brown,978-453-8984,megb@example.com,manager

* Run ls -R and check it against the structure of your project shown
  in Sublime. Should be the same.

* Oops, looks like the last staff file we created was in the root of
  the directory. Lets move it into the Tools directory.

$pwd (Make sure your in the project root dir)
$ mv inventory.csv Tools/.

* Create a notice.txt file in each directory to communicate with the
  employees in each department.

$ pwd (Make sure your in the project root dir)
$ touch notice.txt
$ mv notice.txt Tools/.
$ cp Tools/notice.txt Electrical/.
$ cp Tools/notice.txt Plumbing/read_this.txt (have to tell the
plumbers to actual read the contents, hmmm)
$


* Ok now I want to find all the staff CSV files in my project.
$ pwd (Make sure your in the project root dir)
$ find . -name '*.csv'

This will look for any file that ends in .csv in the current directory
and all descendent directories.

Look for these files in Sublime using it's file search features.

* We forgot what department Jack Sprat works in. Lets find out.

$ pwd (Make sure your in the project root dir)
$ ack "Jack Sprat"
