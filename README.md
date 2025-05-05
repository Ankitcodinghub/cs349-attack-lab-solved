# cs349-attack-lab-solved
**TO GET THIS SOLUTION VISIT:** [CS349 Attack Lab Solved](https://www.ankitcodinghub.com/product/cs349-attack-lab-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;100096&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS349 Attack Lab Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column">
&nbsp;

1 Introduction

This assignment involves generating a total of five attacks on two programs having different security vul- nerabilities. Outcomes you will gain from this lab include:

<ul>
<li>You will learn different ways that attackers can exploit security vulnerabilities when programs do not safeguard themselves well enough against buffer overflows.</li>
<li>Through this, you will get a better understanding of how to write programs that are more secure, as well as some of the features provided by compilers and operating systems to make programs less vulnerable.</li>
<li>You will gain a deeper understanding of the stack and parameter-passing mechanisms of x86-64 machine code.</li>
<li>You will gain a deeper understanding of how x86-64 instructions are encoded.</li>
<li>You will gain more experience with debugging tools such as GDB and OBJDUMP.
Note: In this lab, you will gain firsthand experience with methods used to exploit security weaknesses in operating systems and network servers. Our purpose is to help you learn about the runtime operation of programs and to understand the nature of these security weaknesses so that you can avoid them when you write system code. We do not condone the use of any other form of attack to gain unauthorized access to any system resources.

You will want to study Sections 3.10.3 and 3.10.4 of the CS:APP3e book as reference material for this lab.
</li>
</ul>
</div>
</div>
<div class="layoutArea">
<div class="column">
1

</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
2 Logistics

As usual, this is an individual project. You will generate attacks for target programs that are custom gener- ated for you.

2.1 Getting Files

You can obtain your files by pointing your Web browser at:

<pre>    http://$Attacklab::SERVER_NAME:15513/
</pre>
<pre>INSTRUCTOR: $Attacklab::SERVER_NAME is the machine that runs the
 attacklab servers. You define it in attacklab/Attacklab.pm and in
 attacklab/src/build/driverhdrs.h
</pre>
The server will build your files and return them to your browser in a tar file called targetk.tar, where k is the unique number of your target programs.

Note: It takes a few seconds to build and download your target, so please be patient.

Save the targetk.tar file in a (protected) Linux directory in which you plan to do your work. Then give the command: tar -xvf targetk.tar. This will extract a directory targetk containing the files described below.

You should only download one set of files. If for some reason you download multiple targets, choose one target to work on and delete the rest.

Warning: If you expand your targetk.tar on a PC, by using a utility such as Winzip, or letting your browser do the extraction, you’ll risk resetting permission bits on the executable files.

The files in targetk include:

README.txt: A file describing the contents of the directory

ctarget: An executable program vulnerable to code-injection attacks

rtarget: An executable program vulnerable to return-oriented-programming attacks

cookie.txt: An 8-digit hex code that you will use as a unique identifier in your attacks.

farm.c: The source code of your target’s “gadget farm,” which you will use in generating return-oriented programming attacks.

hex2raw: A utility to generate attack strings.

In the following instructions, we will assume that you have copied the files to a protected local directory,

and that you are executing the programs in that local directory.

</div>
</div>
<div class="layoutArea">
<div class="column">
2

</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="layoutArea">
<div class="column">
2.2 Important Points

Here is a summary of some important rules regarding valid solutions for this lab. These points will not make much sense when you read this document for the first time. They are presented here as a central reference of rules once you get started.

</div>
</div>
<div class="layoutArea">
<div class="column">
3

</div>
<div class="column">
<ul>
<li>You must do the assignment on a machine that is similar to the one that generated your targets.</li>
<li>Your solutions may not use attacks to circumvent the validation code in the programs. Specifically, any address you incorporate into an attack string for use by a ret instruction should be to one of the following destinations:
– The addresses for functions touch1, touch2, or touch3. – The address of your injected code

– The address of one of your gadgets from the gadget farm.
</li>
<li>You may only construct gadgets from file rtarget with addresses ranging between those for func- tions start_farm and end_farm.
Target Programs
</li>
</ul>
</div>
</div>
<div class="layoutArea">
<div class="column">
Both CTARGET and RTARGET read strings from standard input. They do so with the function getbuf defined below:

1 unsigned getbuf() 2{

<ol start="3">
<li>3 &nbsp;char buf[BUFFER_SIZE];</li>
<li>4 &nbsp;Gets(buf);</li>
<li>5 &nbsp;return 1;</li>
</ol>
6}

The function Gets is similar to the standard library function gets—it reads a string from standard input (terminated by ‘\n’ or end-of-file) and stores it (along with a null terminator) at the specified destination. In this code, you can see that the destination is an array buf, declared as having BUFFER_SIZE bytes. At the time your targets were generated, BUFFER_SIZE was a compile-time constant specific to your version of the programs.

Functions Gets() and gets() have no way to determine whether their destination buffers are large enough to store the string they read. They simply copy sequences of bytes, possibly overrunning the bounds of the storage allocated at the destinations.

If the string typed by the user and read by getbuf is sufficiently short, it is clear that getbuf will return 1, as shown by the following execution examples:

</div>
</div>
<div class="layoutArea">
<div class="column">
unix&gt; ./ctarget

</div>
</div>
<div class="layoutArea">
<div class="column">
3

</div>
</div>
</div>
<div class="page" title="Page 4">
<div class="layoutArea">
<div class="column">
Cookie: 0x1a7dd803

Type string: Keep it short!

No exploit. Getbuf returned 0x1 Normal return

Typically an error occurs if you type a long string:

unix&gt; ./ctarget

Cookie: 0x1a7dd803

Type string: This is not a very interesting string, but it has the property … Ouch!: You caused a segmentation fault!

Better luck next time

(Note that the value of the cookie shown will differ from yours.) Program RTARGET will have the same behavior. As the error message indicates, overrunning the buffer typically causes the program state to be corrupted, leading to a memory access error. Your task is to be more clever with the strings you feed CTARGET and RTARGET so that they do more interesting things. These are called exploit strings.

Both CTARGET and RTARGET take several different command line arguments:

-h: Print list of possible command line arguments

-q: Don’t send results to the grading server

-i FILE: Supply input from a file, rather than from standard input

Your exploit strings will typically contain byte values that do not correspond to the ASCII values for printing characters. The program HEX2RAW will enable you to generate these raw strings. See Appendix A for more information on how to use HEX2RAW.

Important points:

• Your exploit string must not contain byte value 0x0a at any intermediate position, since this is the ASCII code for newline (‘\n’). When Gets encounters this byte, it will assume you intended to terminate the string.

• HEX2RAW expects two-digit hex values separated by one or more white spaces. So if you want to create a byte with a hex value of 0, you need to write it as 00. To create the word 0xdeadbeef you should pass “ef be ad de” to HEX2RAW (note the reversal required for little-endian byte ordering).

When you have correctly solved one of the levels, your target program will automatically send a notification to the grading server. For example:

unix&gt; ./hex2raw &lt; ctarget.l2.txt | ./ctarget

Cookie: 0x1a7dd803

Type string:Touch2!: You called touch2(0x1a7dd803) Valid solution for level 2 with target ctarget

PASSED: Sent exploit string to server to be validated. NICE JOB!

</div>
</div>
<div class="layoutArea">
<div class="column">
4

</div>
</div>
</div>
<div class="page" title="Page 5">
<div class="layoutArea">
<div class="column">
Phase Program Level Method Function Points

</div>
</div>
<div class="layoutArea">
<div class="column">
<ol>
<li>1 &nbsp;CTARGET</li>
<li>2 &nbsp;CTARGET</li>
<li>3 &nbsp;CTARGET</li>
<li>4 &nbsp;RTARGET</li>
<li>5 &nbsp;RTARGET</li>
</ol>
</div>
<div class="column">
1 CI 2 CI 3 CI 2 ROP 3 ROP

</div>
<div class="column">
touch1 10 touch2 25 touch3 25 touch2 35 touch3 5

</div>
</div>
<div class="layoutArea">
<div class="column">
CI: Code injection ROP: Return-oriented

</div>
</div>
<div class="layoutArea">
<div class="column">
programming

Figure 1: Summary of attack lab phases

</div>
</div>
<div class="layoutArea">
<div class="column">
The server will test your exploit string to make sure it really works, and it will update the Attacklab score- board page indicating that your userid (listed by your target number for anonymity) has completed this phase.

You can view the scoreboard by pointing your Web browser at

<pre>    http://$Attacklab::SERVER_NAME:15513/scoreboard
</pre>
Unlike the Bomb Lab, there is no penalty for making mistakes in this lab. Feel free to fire away at CTARGET and RTARGET with any strings you like.

IMPORTANT NOTE: You can work on your solution on any Linux machine, but in order to submit your solution, you will need to be running on one of the following machines:

<pre>INSTRUCTOR: Insert the list of the legal domain names that you
 established in buflab/src/config.c.
</pre>
Figure 1 summarizes the five phases of the lab. As can be seen, the first three involve code-injection (CI) attacks on CTARGET, while the last two involve return-oriented-programming (ROP) attacks on RTARGET.

4 Part I: Code Injection Attacks

For the first three phases, your exploit strings will attack CTARGET. This program is set up in a way that the stack positions will be consistent from one run to the next and so that data on the stack can be treated as executable code. These features make the program vulnerable to attacks where the exploit strings contain the byte encodings of executable code.

4.1 Level 1

For Phase 1, you will not inject new code. Instead, your exploit string will redirect the program to execute an existing procedure.

Function getbuf is called within CTARGET by a function test having the following C code: 5

</div>
</div>
</div>
<div class="page" title="Page 6">
<div class="layoutArea">
<div class="column">
1 void test() 2{

<ol start="3">
<li>3 &nbsp;int val;</li>
<li>4 &nbsp;val = getbuf();</li>
<li>5 &nbsp;printf(“No exploit. Getbuf returned 0x%x\n”, val);</li>
</ol>
6}

When getbuf executes its return statement (line 5 of getbuf), the program ordinarily resumes execution within function test (at line 5 of this function). We want to change this behavior. Within the file ctarget, there is code for a function touch1 having the following C representation:

1 void touch1() 2{

<ol start="3">
<li>3 &nbsp;vlevel = 1; /* Part of validation protocol */</li>
<li>4 &nbsp;printf(“Touch1!: You called touch1()\n”);</li>
<li>5 &nbsp;validate(1);</li>
<li>6 &nbsp;exit(0);</li>
</ol>
7}

Your task is to get CTARGET to execute the code for touch1 when getbuf executes its return statement, rather than returning to test. Note that your exploit string may also corrupt parts of the stack not directly related to this stage, but this will not cause a problem, since touch1 causes the program to exit directly.

Some Advice:

</div>
</div>
<div class="layoutArea">
<div class="column">
4.2

</div>
</div>
<div class="layoutArea">
<div class="column">
• •

• •

•

</div>
<div class="column">
All the information you need to devise your exploit string for this level can be determined by exam- iningadisassembledversionofCTARGET.Useobjdump -dtogetthisdissembledversion.

The idea is to position a byte representation of the starting address for touch1 so that the ret instruction at the end of the code for getbuf will transfer control to touch1.

Be careful about byte ordering.

You might want to use GDB to step the program through the last few instructions of getbuf to make sure it is doing the right thing.

The placement of buf within the stack frame for getbuf depends on the value of compile-time constant BUFFER_SIZE, as well the allocation strategy used by GCC. You will need to examine the disassembled code to determine its position.

Level 2

</div>
</div>
<div class="layoutArea">
<div class="column">
Phase 2 involves injecting a small amount of code as part of your exploit string.

Within the file ctarget there is code for a function touch2 having the following C representation:

</div>
</div>
<div class="layoutArea">
<div class="column">
1 void touch2(unsigned val)

</div>
</div>
<div class="layoutArea">
<div class="column">
6

</div>
</div>
</div>
<div class="page" title="Page 7">
<div class="layoutArea">
<div class="column">
4.3

</div>
</div>
<div class="layoutArea">
<div class="column">
2{ 3

4

5

6 7 8 9

10 11 12

</div>
<div class="column">
<pre>vlevel = 2;       /* Part of validation protocol */
if (val == cookie) {
</pre>
</div>
</div>
<div class="layoutArea">
<div class="column">
•

• •

•

•

</div>
<div class="column">
You will want to position a byte representation of the address of your injected code in such a way that ret instruction at the end of the code for getbuf will transfer control to it.

Recall that the first argument to a function is passed in register %rdi.

Your injected code should set the register to your cookie, and then use a ret instruction to transfer

control to the first instruction in touch2.

Do not attempt to use jmp or call instructions in your exploit code. The encodings of destination addresses for these instructions are difficult to formulate. Use ret instructions for all transfers of control, even when you are not returning from a call.

See the discussion in Appendix B on how to use tools to generate the byte-level representations of instruction sequences.

Level 3

</div>
</div>
<div class="layoutArea">
<div class="column">
<pre>    printf("Touch2!:
</pre>
validate(2); }else{

<pre>    printf("Misfire:
</pre>
fail(2); }

</div>
<div class="column">
<pre>You called touch2(0x%.8x)\n", val);
</pre>
<pre>You called touch2(0x%.8x)\n", val);
</pre>
</div>
</div>
<div class="layoutArea">
<div class="column">
exit(0); }

</div>
</div>
<div class="layoutArea">
<div class="column">
Your task is to get CTARGET to execute the code for touch2 rather than returning to test. In this case, however, you must make it appear to touch2 as if you have passed your cookie as its argument.

Some Advice:

</div>
</div>
<div class="layoutArea">
<div class="column">
Phase 3 also involves a code injection attack, but passing a string as argument.

Within the file ctarget there is code for functions hexmatch and touch3 having the following C representations:

1 /* Compare string to hex represention of unsigned value */

</div>
</div>
<div class="layoutArea">
<div class="column">
2 int 3{

4

5

6

7

8 9}

</div>
<div class="column">
<pre>hexmatch(unsigned val, char *sval)
</pre>
<pre>char cbuf[110];
/* Make position of check string unpredictable */
char *s = cbuf + random() % 100;
sprintf(s, "%.8x", val);
return strncmp(sval, s, 9) == 0;
</pre>
</div>
</div>
<div class="layoutArea">
<div class="column">
7

</div>
</div>
</div>
<div class="page" title="Page 8">
<div class="layoutArea">
<div class="column">
5

</div>
<div class="column">
consist of the eight hexadecimal digits (ordered from most to least significant) without a leading “0x.”

<ul>
<li>Recall that a string is represented in C as a sequence of bytes followed by a byte with value 0. Type
“man ascii”onanyLinuxmachinetoseethebyterepresentationsofthecharactersyouneed.
</li>
<li>Your injected code should set register %rdi to the address of this string.</li>
<li>When functions hexmatch and strncmp are called, they push data onto the stack, overwriting portions of memory that held the buffer used by getbuf. As a result, you will need to be careful where you place the string representation of your cookie.
Part II: Return-Oriented Programming
</li>
</ul>
</div>
</div>
<div class="layoutArea">
<div class="column">
<pre>10
11
12
13
14
15
16
17
18
19
20
21
22
</pre>
</div>
<div class="column">
<pre>void touch3(char *sval)
{
</pre>
<pre>    vlevel = 3;       /* Part of validation protocol */
    if (hexmatch(cookie, sval)) {
</pre>
<pre>        printf("Touch3!: You called touch3(\"%s\")\n", sval);
</pre>
<pre>        validate(3);
    } else {
</pre>
<pre>        printf("Misfire: You called touch3(\"%s\")\n", sval);
</pre>
fail(3); }

exit(0); }

</div>
</div>
<div class="layoutArea">
<div class="column">
Your task is to get CTARGET to execute the code for touch3 rather than returning to test. You must make it appear to touch3 as if you have passed a string representation of your cookie as its argument.

Some Advice:

• Youwillneedtoincludeastringrepresentationofyourcookieinyourexploitstring.Thestringshould

</div>
</div>
<div class="layoutArea">
<div class="column">
Performing code-injection attacks on program RTARGET is much more difficult than it is for CTARGET, because it uses two techniques to thwart such attacks:

<ul>
<li>It uses randomization so that the stack positions differ from one run to another. This makes it impos- sible to determine where your injected code will be located.</li>
<li>It marks the section of memory holding the stack as nonexecutable, so even if you could set the program counter to the start of your injected code, the program would fail with a segmentation fault.
Fortunately, clever people have devised strategies for getting useful things done in a program by executing existing code, rather than injecting new code. The most general form of this is referred to as return-oriented programming (ROP) [1, 2]. The strategy with ROP is to identify byte sequences within an existing program that consist of one or more instructions followed by the instruction ret. Such a segment is referred to as a
</li>
</ul>
</div>
</div>
<div class="layoutArea">
<div class="column">
8

</div>
</div>
</div>
<div class="page" title="Page 9">
<div class="section">
<div class="layoutArea">
<div class="column">
%rsp

</div>
</div>
<div class="layoutArea">
<div class="column">
Stack

</div>
</div>
<div class="layoutArea">
<div class="column">
Gadget n code c3

</div>
</div>
<table>
<tbody>
<tr>
<td></td>
</tr>
<tr>
<td>
<div class="layoutArea">
<div class="column">
  

</div>
</div>
</td>
</tr>
<tr>
<td></td>
</tr>
<tr>
<td></td>
</tr>
</tbody>
</table>
<div class="layoutArea">
<div class="column">
Gadget 2 code c3

</div>
</div>
<div class="layoutArea">
<div class="column">
Gadget 1 code c3

</div>
</div>
</div>
<div class="layoutArea">
<div class="column">
Figure 2: Setting up sequence of gadgets for execution. Byte value 0xc3 encodes the ret instruction.

gadget. Figure 2 illustrates how the stack can be set up to execute a sequence of n gadgets. In this figure, the stack contains a sequence of gadget addresses. Each gadget consists of a series of instruction bytes, with the final one being 0xc3, encoding the ret instruction. When the program executes a ret instruction starting with this configuration, it will initiate a chain of gadget executions, with the ret instruction at the end of each gadget causing the program to jump to the beginning of the next.

A gadget can make use of code corresponding to assembly-language statements generated by the compiler, especially ones at the ends of functions. In practice, there may be some useful gadgets of this form, but not enough to implement many important operations. For example, it is highly unlikely that a compiled function would have popq %rdi as its last instruction before ret. Fortunately, with a byte-oriented instruction set, such as x86-64, a gadget can often be found by extracting patterns from other parts of the instruction byte sequence.

For example, one version of rtarget contains code generated for the following C function:

<pre>void setval_210(unsigned *p)
{
</pre>
<pre>    *p = 3347663060U;
}
</pre>
The chances of this function being useful for attacking a system seem pretty slim. But, the disassembled machine code for this function shows an interesting byte sequence:

<pre>0000000000400f15 &lt;setval_210&gt;:
  400f15:       c7 07 d4 48 89 c7       movl   $0xc78948d4,(%rdi)
  400f1b:       c3                      retq
</pre>
The byte sequence 48 89 c7 encodes the instruction movq %rax, %rdi. (See Figure 3A for the encodings of useful movq instructions.) This sequence is followed by byte value c3, which encodes the ret instruction. The function starts at address 0x400f15, and the sequence starts on the fourth byte of the function. Thus, this code contains a gadget, having a starting address of 0x400f18, that will copy the 64-bit value in register %rax to register %rdi.

</div>
</div>
<div class="layoutArea">
<div class="column">
9

</div>
</div>
</div>
<div class="page" title="Page 10">
<div class="layoutArea">
<div class="column">
Your code for RTARGET contains a number of functions similar to the setval_210 function shown above in a region we refer to as the gadget farm. Your job will be to identify useful gadgets in the gadget farm and use these to perform attacks similar to those you did in Phases 2 and 3.

Important: The gadget farm is demarcated by functions start_farm and end_farm in your copy of rtarget. Do not attempt to construct gadgets from other portions of the program code.

5.1 Level 2

For Phase 4, you will repeat the attack of Phase 2, but do so on program RTARGET using gadgets from your gadget farm. You can construct your solution using gadgets consisting of the following instruction types, and using only the first eight x86-64 registers (%rax–%rdi).

movq : The codes for these are shown in Figure 3A.

popq : The codes for these are shown in Figure 3B.

ret : This instruction is encoded by the single byte 0xc3.

nop : This instruction (pronounced “no op,” which is short for “no operation”) is encoded by the single byte 0x90. Its only effect is to cause the program counter to be incremented by 1.

Some Advice:

</div>
</div>
<div class="layoutArea">
<div class="column">
5.2

</div>
</div>
<div class="layoutArea">
<div class="column">
•

• •

</div>
<div class="column">
All the gadgets you need can be found in the region of the code for rtarget demarcated by the functions start_farm and mid_farm.

You can do this attack with just two gadgets.

When a gadget uses a popq instruction, it will pop data from the stack. As a result, your exploit string will contain a combination of gadget addresses and data.

Level 3

</div>
</div>
<div class="layoutArea">
<div class="column">
Before you take on the Phase 5, pause to consider what you have accomplished so far. In Phases 2 and 3, you caused a program to execute machine code of your own design. If CTARGET had been a network server, you could have injected your own code into a distant machine. In Phase 4, you circumvented two of the main devices modern systems use to thwart buffer overflow attacks. Although you did not inject your own code, you were able inject a type of program that operates by stitching together sequences of existing code. You have also gotten 95/100 points for the lab. That’s a good score. If you have other pressing obligations consider stopping right now.

Phase 5 requires you to do an ROP attack on RTARGET to invoke function touch3 with a pointer to a string representation of your cookie. That may not seem significantly more difficult than using an ROP attack to invoke touch2, except that we have made it so. Moreover, Phase 5 counts for only 5 points, which is not a true measure of the effort it will require. Think of it as more an extra credit problem for those who want to go beyond the normal expectations for the course.

</div>
</div>
<div class="layoutArea">
<div class="column">
10

</div>
</div>
</div>
<div class="page" title="Page 11">
<div class="layoutArea">
<div class="column">
A. Encodings of movq instructions

movq S, D Source

S %rax %rcx %rax 4889c0 4889c1 %rcx 4889c8 4889c9 %rdx 4889d0 4889d1 %rbx 4889d8 4889d9 %rsp 4889e0 4889e1 %rbp 4889e8 4889e9 %rsi 4889f0 4889f1 %rdi 4889f8 4889f9

B. Encodings of popq instructions Operation

</div>
<div class="column">
Destination D

%rdx %rbx %rsp %rbp %rsi %rdi

4889c2 4889c3 4889c4 4889c5 4889c6 4889c7 4889ca 4889cb 4889cc 4889cd 4889ce 4889cf 4889d2 4889d3 4889d4 4889d5 4889d6 4889d7 4889da 4889db 4889dc 4889dd 4889de 4889df 4889e2 4889e3 4889e4 4889e5 4889e6 4889e7 4889ea 4889eb 4889ec 4889ed 4889ee 4889ef 4889f2 4889f3 4889f4 4889f5 4889f6 4889f7 4889fa 4889fb 4889fc 4889fd 4889fe 4889ff

</div>
</div>
<div class="layoutArea">
<div class="column">
Register R

%rax %rcx %rdx %rbx %rsp %rbp %rsi %rdi

</div>
</div>
<div class="layoutArea">
<div class="column">
popqR 58 59 5a 5b 5c 5d 5e 5f C. Encodings of movl instructions

movl S, D

Source Destination D

S %eax %ecx %edx %ebx %esp %ebp %esi %edi %eax 89c0 89c1 89c2 89c3 89c4 89c5 89c6 89c7 %ecx 89c8 89c9 89ca 89cb 89cc 89cd 89ce 89cf %edx 89d0 89d1 89d2 89d3 89d4 89d5 89d6 89d7 %ebx 89d8 89d9 89da 89db 89dc 89dd 89de 89df %esp 89e0 89e1 89e2 89e3 89e4 89e5 89e6 89e7 %ebp 89e8 89e9 89ea 89eb 89ec 89ed 89ee 89ef %esi 89f0 89f1 89f2 89f3 89f4 89f5 89f6 89f7 %edi 89f8 89f9 89fa 89fb 89fc 89fd 89fe 89ff

D. Encodings of 2-byte functional nop instructions

Operation Register R

%al %cl %dl %bl

andb R,R 20c0 20c9 20d2 20db orb R, R 08 c0 08 c9 08 d2 08 db cmpb R,R 38c0 38c9 38d2 38db testb R,R 84c0 84c9 84d2 84db

Figure 3: Byte encodings of instructions. All values are shown in hexadecimal.

</div>
</div>
<div class="layoutArea">
<div class="column">
11

</div>
</div>
</div>
<div class="page" title="Page 12">
<div class="layoutArea">
<div class="column">
To solve Phase 5, you can use gadgets in the region of the code in rtarget demarcated by functions start_farm and end_farm. In addition to the gadgets used in Phase 4, this expanded farm includes the encodings of different movl instructions, as shown in Figure 3C. The byte sequences in this part of the farm also contain 2-byte instructions that serve as functional nops, i.e., they do not change any register or memoryvalues.Theseincludeinstructions,showninFigure3D,suchasandb %al,%al,thatoperateon the low-order bytes of some of the registers but do not change their values.

Some Advice:

• You’ll want to review the effect a movl instruction has on the upper 4 bytes of a register, as is described on page 183 of the text.

• The official solution requires eight gadgets (not all of which are unique). Good luck and have fun!

A Using HEX2RAW

HEX2RAW takes as input a hex-formatted string. In this format, each byte value is represented by two hex digits. For example, the string “012345” could be entered in hex format as “30 31 32 33 34 35 00.” (Recall that the ASCII code for decimal digit x is 0x3x, and that the end of a string is indicated by a null byte.)

The hex characters you pass to HEX2RAW should be separated by whitespace (blanks or newlines). We recommend separating different parts of your exploit string with newlines while you’re working on it. HEX2RAW supports C-style block comments, so you can mark off sections of your exploit string. For example:

48 c7 c1 f0 11 40 00 /* mov $0x40011f0,%rcx */

Be sure to leave space around both the starting and ending comment strings (“/*”, “*/”), so that the

comments will be properly ignored.

If you generate a hex-formatted exploit string in the file exploit.txt, you can apply the raw string to CTARGET or RTARGET in several different ways:

1. You can set up a series of pipes to pass the string through HEX2RAW.

unix&gt; cat exploit.txt | ./hex2raw | ./ctarget 2. You can store the raw string in a file and use I/O redirection:

unix&gt; ./hex2raw &lt; exploit.txt &gt; exploit-raw.txt unix&gt; ./ctarget &lt; exploit-raw.txt

This approach can also be used when running from within GDB: 12

</div>
</div>
</div>
<div class="page" title="Page 13">
<div class="layoutArea">
<div class="column">
B

</div>
<div class="column">
unix&gt; gdb ctarget

(gdb) run &lt; exploit-raw.txt

3. You can store the raw string in a file and provide the file name as a command-line argument:

unix&gt; ./hex2raw &lt; exploit.txt &gt; exploit-raw.txt unix&gt; ./ctarget -i exploit-raw.txt

This approach also can be used when running from within GDB.

Generating Byte Codes

</div>
</div>
<div class="layoutArea">
<div class="column">
Using GCC as an assembler and OBJDUMP as a disassembler makes it convenient to generate the byte codes for instruction sequences. For example, suppose you write a file example.s containing the following assembly code:

<pre># Example of hand-generated assembly code
</pre>
</div>
</div>
<div class="layoutArea">
<div class="column">
<pre>pushq   $0xabcdef
addq    $17,%rax
movl    %eax,%edx
</pre>
</div>
<div class="column">
<pre># Push value onto stack
# Add 17 to %rax
# Copy lower 32 bits to %edx
</pre>
</div>
</div>
<div class="layoutArea">
<div class="column">
The code can contain a mixture of instructions and data. Anything to the right of a ‘#’ character is a comment.

You can now assemble and disassemble this file:

unix&gt; gcc -c example.s

unix&gt; objdump -d example.o &gt; example.d

The generated file example.d contains the following: example.o: file format elf64-x86-64

<pre>Disassembly of section .text:
</pre>
</div>
</div>
<div class="layoutArea">
<div class="column">
<pre>0000000000000000 &lt;.text&gt;:
   0: 68 ef cd ab 00
   5: 48 83 c0 11
   9: 89 c2
</pre>
</div>
<div class="column">
<pre>pushq  $0xabcdef
add    $0x11,%rax
mov    %eax,%edx
</pre>
</div>
</div>
<div class="layoutArea">
<div class="column">
The lines at the bottom show the machine code generated from the assembly language instructions. Each line has a hexadecimal number on the left indicating the instruction’s starting address (starting with 0), while

</div>
</div>
<div class="layoutArea">
<div class="column">
13

</div>
</div>
</div>
<div class="page" title="Page 14">
<div class="layoutArea">
<div class="column">
the hex digits after the ‘:’ character indicate the byte codes for the instruction. Thus, we can see that the instructionpush $0xABCDEFhashex-formattedbytecode68 ef cd ab 00.

From this file, you can get the byte sequence for the code:

<pre>68 ef cd ab 00 48 83 c0 11 89 c2
</pre>
This string can then be passed through HEX2RAW to generate an input string for the target programs.. Alter- natively, you can edit example.d to omit extraneous values and to contain C-style comments for readability, yielding:

<pre>   68 ef cd ab 00   /* pushq  $0xabcdef  */
   48 83 c0 11      /* add    $0x11,%rax */
   89 c2            /* mov    %eax,%edx  */
</pre>
This is also a valid input you can pass through HEX2RAW before sending to one of the target programs.

References

[1] R. Roemer, E. Buchanan, H. Shacham, and S. Savage. Return-oriented programming: Systems, lan- guages, and applications. ACM Transactions on Information System Security, 15(1):2:1–2:34, March 2012.

[2] E. J. Schwartz, T. Avgerinos, and D. Brumley. Q: Exploit hardening made easy. In USENIX Security Symposium, 2011.

</div>
</div>
<div class="layoutArea">
<div class="column">
14

</div>
</div>
</div>
