partner1_username, partner2_username

# Project 1: Boolean Logic

## Submitter details

- Partner1FirstName Partner1LastName, ID 011111111, partner1_email@mail.huji.ac.il
- Partner2FirstName Partner2LastName, ID 022222222, partner2_email@mail.huji.ac.il

## Submitted Files

- README.md: This file.
- And.hdl:
- Not.hdl:
- Or.hdl:
- Xor.hdl:
- Mux.hdl:
- DMux.hdl:
- Not16.hdl:
- And16.hdl:
- Or16.hdl:
- Mux16.hdl:
- Or8Way.hdl:
- Mux4Way16.hdl:
- Mux8Way16.hdl:
- DMux4Way.hdl:
- DMux8Way.hdl:

## Remarks

- You should submit a zip file with a README and the following files:
  README.md, Not.hdl, And.hdl, Or.hdl, Xor.hdl, Mux.hdl, DMux.hdl, Not16.hdl,
  And16.hdl, Or16.hdl, Mux16.hdl, Or8Way.hdl, Mux4Way16.hdl, Mux8Way16.hdl,
  DMux4Way.hdl, DMux8Way.hdl
- You can create & use new chips, but should include them in the submission.
- Include other files required by your project, if there are any.
- The submission should not contain any folder.
- The README.md file must contain the following:
  - In the first line: login(s) of the author(s), separated by commas and
    nothing else! If you work alone, do not include a comma.
    Logins should be identical to the names of your home folders and are
    case-sensitive.
  - Name(s), email(s) and ID(s) of the project's author(s).
  - Any remarks you have about your submission.

## Background

A typical computer architecture is based on a set of elementary logic gates
like And, Or, Mux, etc., as well as their bit-wise versions And16, Or16,
Mux16, etc. (assuming a 16-bit machine). This project engages you in the
construction of a typical set of basic logic gates. These gates form the
elementary building blocks from which more complex chips will be later
constructed.

## Objective

Build all the logic gates given in this folder, yielding a basic chip-set.
The only building blocks that you can use in this project are primitive Nand
gates and the composite gates that you will gradually build on top of them.

## Project

For each chip, we supply a skeletal .hdl file with a place holder for a missing
implementation part. In addition, for each chip we supply a .tst script that
instructs the hardware simulator how to test it, and a .cmp ("compare file")
containing the correct output that this test should generate. Your job is to
complete and test the supplied skeletal .hdl files.

Proceed in the following manner:

- Write an implementation for chip Xxx in Xxx.hdl,
- Test your implementation by loading Xxx.tst into the HardwareSimulator,
- If you have any errors, fix them and go back to the first step.

We recommend implementing all the gates in this project in the order in which
they appear in Chapter 1:
Not, And, Or, Xor, Mux, DMux, Not16, And16, Or16, Mux16, Or8Way, Mux4Way16,
Mux8Way16, DMux4Way, DMux8Way.
The book and accompanying video lectures contain very heavy hints with regards
to almost all of these chips.

If you've downloaded the Nand2Tetris Software Suite, you will find the supplied
hardware simulator and all the necessary project files in the nand2tetris/tools
folder and in the nand2tetris/projects/01 folder, respectively. To get
acquainted with the hardware simulator, see the Hardware Simulator Tutorial.

## Built-in chips

The Nand gate is considered primitive and thus there is no need to implement it:
whenever a Nand chip-part is encountered in your HDL code, the simulator
automatically invokes the built-in tools/builtInChips/Nand.hdl implementation.

Note that the supplied hardware simulator features built-in implementations of
all these chips. Therefore, you can use any one of these chips before
implementing it: the simulator will automatically invoke their built-in
versions.

For example, consider the supplied skeletal Mux.hdl program. Suppose that for
one reason or another you did not complete the implementation of Mux, but you
still want to use Mux chips as internal parts in other chip designs. You can
easily do so, thanks to the following convention. If the simulator fails to
find a Mux.hdl file in the current directory, it automatically invokes the
built-in Mux implementation, which is part of the supplied simulator's
environment. This built-in Mux implementation has the same interface and
functionality as those of the Mux chip described in the book. Thus, if you want
the simulator to ignore one or more of your chip implementations, rename the
corresponding chiPname.hdl file, or remove it from the directory. When you are
ready to develop this chip in HDL, put the file chipName.hdl back in the
directory, and proceed to edit it with your HDL code.

This file is part of nand2tetris, as taught in The Hebrew University, and
was written by Aviv Yaish. It is an extension to the specifications given
[here](https://www.nand2tetris.org) (Shimon Schocken and Noam Nisan, 2017),
as allowed by the Creative Common Attribution-NonCommercial-ShareAlike 3.0
Unported [License](https://creativecommons.org/licenses/by-nc-sa/3.0/).