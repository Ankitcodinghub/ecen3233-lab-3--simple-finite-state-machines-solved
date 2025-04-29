# ecen3233-lab-3--simple-finite-state-machines-solved
**TO GET THIS SOLUTION VISIT:** [ECEN3233 Lab 3- Simple Finite State Machines Solved](https://www.ankitcodinghub.com/product/ecen3233-lab-3-simple-finite-state-machines-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;113255&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;ECEN3233 Lab 3- Simple Finite State Machines Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

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
1. Introduction

This is a somewhat simpler laboratory but a crucial one. In this laboratory we will get our rst introduction to sequential logic and how this works. Although sequential logic is typically a lot smaller than combinational designs, it is incredibly valuable in that it provides most of the intelligence within digital logic. That is, most computing devices have several million Boolean gates on them, but without some mechanism to control the logic, it would never work.

In this laboratory, we are going to use an idea that has been in a popular textbook that is a little older but we are going to give a new twist to it [1]. Again, although this laboratory is relatively simple the importance of this laboratory to later work will be crucial. So, it is important to try to understand the procedure in creating these systems.

2. Background

Until now, we have only designed combinational circuits. In this lab we will start with circuits that have distinct states. We once again use SystemVerilog to specify our design. As discussed in class, since FSMs are di erent in terms of their feedback, they should be integrated within a Hardware Descriptive Language (HDL) a little di erently to allow the synthesizer to properly design them.

In this lab, you’ll design a nite state machine to control the taillights of a 1965 Ford Thunderbird [1]. There are three lights on each side that operate in sequence to indicate the direction of a turn. Figure 1 shows the tail lights and Figure 2 shows the ashing sequence for (a) left turns and (b) right turns.

Both the car and the ashing sequence occur in various varieties in other cars as well as other vehicles (e.g., on bicycle lights). Nevertheless, this is a great exercise to learn how to design a simple Finite State Machine (FSM).

2.1 Baseline Design

Let us start with designing the state transition diagram for this FSM. Give each state a name and indicate the values of the six outputs LC, LB, LA, RA, RB, and RC in each state. Your FSM should take three inputs: reset, left, and right. The circuit should have the following properties:

On reset, the FSM should enter a state with all lights o .

When you press left, you should see LA, then LA and LB, then LA, LB, and LC, then nally all lights o again.

This pattern should occur even if you release left during the sequence. If left is still down when you return to the lights o state, the pattern should repeat.

The operation when right is active should be similar except with RA, RB and RC.

It is up to you to decide what to do if the user makes left and right simultaneously true; make a choice to keep your design easy.

The job of an FSM is to do three things:

Figure 1: Thunderbird Tail Lights [1]

Figure 2: Flashing Sequence (shaded lights are illuminated) [1]

1. Determine the next state from the present state, and the inputs (next state logic).

2. Realize the output function based on the present state and the inputs if a Mealy FSM is used (outputlogic).

3. Advance from the present state to next state when a clock event arrives (state register).

As discussed in class, the state-machine diagram is an optional step, however, the state transition table is an integral and required step to start. You should start designing your state-transition table. Essentially, a state-transition table is a state-machine diagram in a table form, so that we can use our knowledge in designing combinatorial circuits to derive the Boolean equations for next state logic and output logic.

2.2 FSMs in SystemVerilog

Again, as discussed in class, synthesis engines must resort to methodologies that allow them to integrate FSMs into hardware. There is an extensive amount of literature on the integration of FSMs, but it basically boils down to the following items within the HDL. These items are basically the same for other HDLs including VHDL and Verilog.

Inside the SystemVerilog le, each FSM has to have the following distinct and separate items. the state register (where clock moves the next state to the present state) the next state logic (where the next state is determined by the present state and inputs) the output logic (where the outputs are determined by the present state and inputs) works the best.

Also discussed in class, the output logic and the next-state logic can be separate, but I think you will have more luck and less problems if you combine both of these elements into one item. We discussed this in class rather extensively. Normally, engineers like to have separate output and next-state logic inside a HDL as it saves space, but I believe it possibly leads to missing an output. I will leave the choice up to you. The textbook also discusses this rather extensive in Chapter 4 [2].

It is also good practice to use a naming style that clearly identi es the signals that are registered. If you want to know how every registered signal is connected. Therefore, you should name your states accordingly and not something ambiguous like state1.

One of the best practices for debugging FSMs is to also make sure you display your CURRENT_STATE and NEXT_STATE variables on the waveform. This is vital in debugging your FSM and making sure the output module clk_div (input logic clk, input logic rst, output logic clk_en); logic [23:0] clk_count;

always_ff @(posedge clk)

//posedge defines a rising edge (transition from 0 to 1) begin

if (rst)

clk_count &lt;= 24’h0;

else clk_count &lt;= clk_count + 1;

end

assign clk_en = clk_count[23]; endmodule

Figure 3: Clock Divider SystemVerilog File

occurs correctly. You can also output these variables to a display, such as a 7-segment display, and many engineers have this integrated into special debugging con gurations for a digital design.

2.3 Asynchronous Events and Synchronizing the Clock

The problem is that compared to the speed of the FPGA the change in a push button is extremely slow (in fact more than a million times slower). During the slow transition the FPGA will see many fast occurring transitions, and would interpret each of them as a clock edge. This is known as ‘bounce’, and usually specialized circuits (and sampling techniques) are used to prevent this. In any case, using the push buttons is not a very safe way of generating the clock.

Now we have a di erent practical problem: the clock is too fast. The 125 MHz means that every clock period is 8 nanoseconds long. The entire blinking sequence would be then 40 ns. This is a very short time: light travels less than 250 meters during that time. If we want to see our sequence, we need to nd a way to dramatically slow down the circuit.

This can be achieved by two means. Either we implement a clock divider circuit that divides the clock by a few million times, or we can generate an enable signal every few million cycles, and then use this enable signal to control our next state transition. We will employ the former for this laboratory.

In this exercise, we will give you a small clk_div circuit that takes in the same clk and rst signals, and generates a clk_en edge signal every 8,388,608 cycles (or every 223 cycles). Considering that the main clock frequency is 125,000,000 cycles per second, this means a clk_en signal is generated every 0.06711 seconds or 67.11 ms. This is a realistic clock to our light controller in action. The SystemVerilog is shown in Figure 3

The idea is pretty simple, we increment a 24-bit counter (called clk_div) at every clock, and set the clk_en to 1 when the most-signi cant bit (MSB) of the counter s 1. By increasing the counter size you can change the division factor as you please. Use this new clk_en as your clock for your FSM. Now all we have to do is to choose which buttons on the board we want to use for the control, and which LEDs we will use as taillights.

2.4 Alternate Design

We also want to make several modi cations to this lab to give some di erent approaches. Therefore, you should also incorporate the following items into your design as a modi cation of the baseline laboratory.

If both left and right are both asserted, you should have both lights (e.g., LA, LB, and LC) ash on and o . This would be similar to a hazard light in your car.

The Ford Mustang’s hazard lights work like the normal hazards except they produce them in sequence like our normal baseline lab. That is, you should have them do the following when in hazard mode: 1.) LA and RA 2.) add LB and RB and nally 3.) add LC and RC. You can see them on the following YouTube video: https://youtu.be/5azgaPDvPDk.

You should download the les in this lab from Canvas. In the distribution is the normal top_demo similar to Laboratory 1. A template FSM SystemVerilog le is given and you can use it to modify your FSM for this laboratory. As mentioned in previous labs, please make sure you adequately simulate your design with a testbench. Do not go to implementation without simulating your design completely on your laptop or desktop at home.

Both the clock divider and template Finite State Machine SystemVerilog (SV) le are given to you in your zip les. There are also separate DO les so you can run both easily. You will need, as indicated previously, a complete a state-transition table for your design. Although it is tempting to do this without writing it down, it is highly advisable to write it down. Then, just update your FSM SV le accordingly.

2.5 Power, Performance and Area (PPA)

For this laboratory, we are going to analyze the design with the same PPA as in previous labs. That is, you should analyze your design for Power, Performance and Area. Again, as with any digital design, engineers use PPA to assess the level of di culty, challenge, and e ort needed for a design. You should also generate a schematic of your design by using the tools within Vivado – this should be an easy click and generate option. If you cannot nd this, please let us know.

3. Tasks

This is a simple lab and just involves implementing the Finite State Machine for both the baseline and alternate design (i.e., with hazards). Of all our labs, this laboratory is probably the easiest, but FSMs are essential to our project; therefore, make sure you do your best to understand how to implement FSMs as well as debug issues and/or errors that occur.

The main tasks for this laboratory will be the following elements:

1. Design the simple FSM that lights up the LEDs for a Left and Right turn.

3. After verifying your design with a testbench in ModelSim, implement your design on the DSDB boardand use the LEDs for your lights. You can assign any 3 LEDs for left and 3 LEDs for right turns. You should use the switches for initiating a Left, Right, or Hazard condition making sure that multiple operations do not occur simultaneously. You should also implement a reset for your FSM.

4. Document your FSM diagram with paper/pencil or a program such as graphviz. It would also be advantageous to have an implementation on paper (i.e., using D- ip ops) as well as the schematic what is produced from Vivado.

5. Use the push buttons, switches, and LEDs to help you input your plaintext as well as debug operationand prove that your design works on your DSDB board.

6. You should also analyze the PPA impact on your design.

3.1 Submission

You should electronically hand in your HDL (all les that you want us to see) into Canvas. You should also take a printout of your waveform from your ModelSim simulation and annotate it correctly. Only one of your team members should upload the les and/or lab report. Your code should be readable and well-documented. In addition, please turn in additional test cases or any other added item that you used. Please also remember to document everything in your Lab Report using the information found in the Grading Rubric.

3.2 Hints/Tips

One of the challenges in this lab is that the clock for the FSM is so much slower than the clock for the FPGA. This will allow you to use a clock that is faster. Do not forget to output the CURRENT_STATE and NEXT_STATE to your waveform to check where you are with your state. It would be highly advisable to also simulate the FSM with a separate testbench. Then, create a top-level module (i.e., digital design) that incorporates the clk_en and the FSM and simulate with a separate testbench than the clk_en and the FSM. The Graphical User Interface or GUI is really useful in debugging your FSM. Another great hint is to also output both state variables (e.g., as output logic instead of logic and then send that output to the board somehow (e.g., 7-segment display).

As in previous labs, it is highly advisable to do all your simulation at home before you get to ENDV. The testbench methodology is so crucial to the implementation and saves you so much time. Otherwise, you are debugging both the implementation and design and just wasting time. So, make sure you have your design completely working within a testbench before you come to ENDV 350.

Also remember there are two types of Finite State Machine (FSM) designs as discussed in class: Mealy and Moore. This lab will implement a Moore-style FSM and you should de ne the output per each state. The book does this a little di erently within SystemVerilog and its far easier to de ne the output in each next-state as recommended, as mentioned in class.

Also, remember you can use the switches, LEDs, push buttons and 7-segment displays to help you debug the implementation. These debugging elements are very crucial to debugging your design. Also, feel free to play with the clock divider to speed or slow things down. If you get tricky, you could easily output the time (i.e. in ms or seconds) that the clock is working at on the 7-segment display, which would be a cool extra-credit option.

References

[1] John F. Wakerly, Digital design – principles and practices, Prentice Hall Series in computer engineering. Prentice Hall, USA, 4th edition, 2005.
