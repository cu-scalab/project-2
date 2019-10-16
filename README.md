# Part A

In this part you are required to build a basic mips32 assembler for well-formatted assembly inputs. Following are the useful instructions you need to follow:-

1. All input instructions will be provided on separate lines with no spaces before.
2. Instructions are the instruction set (subset of mips) as mentioned in `zybooks 5.1`
3. Instructions for translation are mentioned in `zybooks 5.4`
4. Output should be one line per binary, no preluded spacing. 

Using the assembler you built, encode the following instructions:-
1. add t3, t5, t7
2. lw t4, 0x8(t8)
3. beq t4, t3, 0x100

Using the assembler you built, encode the following instructions:-
1. Decode instruction: 10101101010010010000000000010000


In your report include the results of encoding and decoding.

`Note`:  You should write this as binary, not as 0/1 ascii characters. Each language has a way to read/write raw binary to files. They will possibly not be human readable. http://www.mrc.uidaho.edu/mrc/people/jff/digital/MIPSir.html is a good source for instruction format.


# Part B

In this part you are required to simulate a CPU (as seen in `zybooks 5.4`). Follow the following instructions:-

1. You are required to follow MVC(Model View Controller) design pattern for your software architecture. You can check what MVC is at https://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93controller
2. For the Model, you should use a good abstraction of the CPU, e.g. separate logic blocks as objects. 
3. "Controller" will allow different granularities of runtime. You are required to have a version of the controller that runs the entire program, however you may wish to implement a "single-step" controller that does one at a time with press of keyboard button.
4. "View" - at least one "text" view that will display a "scoreboard" that shows the contents of PC, registers, and memory; also of logic block statistics - they should use the observer pattern to implement this. `Note:` The view is expected to update every cycle. For the text view, that means it should print the scoreboard on every cycle.
5. You should track # cycles for a given program. Also, you should track ALU arithmetic operations (how many add, sub, etc ops). `Note`: Some instructions besides "add" use add. example is beq; this counts as an ALU arithmetic op, incrementing the PC does not.
6. You should track # of memory reads/writes too. 
7. The control should track the # of each individual instruction.


# Things to avoid
You should not just have one long "main".  You should use structures appropriately. You are allowed to use C++ only if you have had Brian Malloy's 2-D game design experience. 


# General Requirements
a. You can work in teams of 2. No discussion with other teams are allowed.

b. You should get started early. 

c. You are required to design memory well because we are going to plug the cache in later. 

d. You should include a readme with YOUR NAMES and documentation about their project; e.g. design decisions and specifics. 

e. You should use object-oriented design principles.  

# Notes about Output
You are free to use language of your choice, however, you should create a makefile with "all" and "clean" targets - all will compile all code into executables "masm" - mips assembler, and "smolmips" - the simulator. Simulator should take one argument - the program to simulate. You can add additional arguments or whatever (for single stepping etc), but `./smolmips myprog.bin` should give the expected behavior, where myprog.bin is some output of the assembler. make + that command should be enough to run the program - no other script setups.

# Language
You are encouraged to use Java because it is easy to express object oriented designs. You can also use C if you know how to use object-oriented principles in C. If you don't you will lose points. You can also use C++ if you have experience with Brian Malloy's 2-D game design. You are not supposed to use libraries but the default builtin.

# Bonus and Extra Points
a. If anyone is super eager, you can earn up to 10 extra points if they create a GUI view. 

b. Also up to 20 points if you create a pipelined version, but the pipelined version scoredboard must track each stage.

# Deadline
The deadline to complete the project is 8th of Nov 2019
