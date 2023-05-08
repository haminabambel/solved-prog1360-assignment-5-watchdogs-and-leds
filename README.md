Download Link: https://assignmentchef.com/product/solved-prog1360-assignment-5-watchdogs-and-leds
<br>
<h2></h2>

<ul>

 <li>Interact with the LEDs directly using memory</li>

 <li>Implement and demonstrate the use of the watchdog</li>

 <li>Structure your code</li>

 <li>Major Tasks</li>

</ul>

<h3>Demonstration – Building on Labs</h3>

This assignment builds on the labs and assignments so far.

The Demonstration section of this document outlines the items you are required to show.

<h2>Tasks</h2>

You will revisit the blinking lights game of Assignment 3 and make modifications. Modifications to make:

<ol>

 <li>Replace the calls to BSP_LED_Toggle / LED_ON / LED_OFF with direct memory access as shown in Lab 9.</li>

 <li>Modify the winning code (blink all lights on and off twice) with direct memory access, changing the state of all lights with single calls (all on / all off) instead of individual calls.</li>

</ol>

Additions to make:

Create a new test item in the menu (the one we normally access with minicom) to demonstrate that the hardware watchdog works. Requirements:

<ol>

 <li>Initialize and start the watchdog from the C code as shown in the lab</li>

 <li>Experiment with the prescaler and reload values to determine the watchdog duration. Make this duration configurable in the call to your C code.</li>

 <li>This function will blink the LEDs in a continuous loop using direct memory access</li>

 <li>If the user button is not pressed, refresh the watchdog between LED blinks</li>

 <li>If the user button is pressed, don’t refresh the watchdog, but continue blinking the LEDs. A properly configured watchdog will result in the board rebooting after the watchdog timer has expired.</li>

</ol>

Given the command below (where xx is your initials)

xxWatch duration delay

your board will execute the blinking light loop with the watchdog enabled for the duration you specify. You will need to determine what the units of duration are.

Where necessary, you can still use the busy_delay. You may have to refresh the watchdog during the busy delay if the timeout is less than the delay.

<h3>Requirements</h3>

<ul>

 <li>Only the watchdog initialization is to be implemented in your C hook code.</li>

 <li>You may use library functions from the stm32 code to parse input.</li>

 <li>You must use direct memory access to manipulate the LEDs</li>

 <li>It is very important that you structure your code cleanly for this assignment.</li>

 <li>You must name all functions and adapt any menu help instructions appropriately.</li>

 <li>You will have to determine how the watchdog timeout duration is calculated. (This may be useful to research)</li>

 <li>On starting the game, ensure that all lights are first turned off.</li>

</ul>

<h2>Demonstration</h2>

Please note that you must be prepared before offering to demonstrate your code. You must demonstrate the code that you have submitted to the eConestoga dropbox.

For this assignment, you will demonstrate the following items. You may use a lab PC or your own. If needed, you may use a classmate’s VM, but you MUST run your own code and only your own code. You must demonstrate in your regularly scheduled lab period. If you demonstrate modified code, you will receive a late penalty according to how long it has been since the dropbox deadline.

<ol>

 <li>Your xx_hook.c and xx_asm.s code as taken directly from the drop box compiles.</li>

 <li>Your code deploys with sudo make program.</li>

 <li>Your code runs with no parameters provided (sensible defaults).</li>

 <li>Your code runs as specified.</li>

 <li>You can demonstrate both cases – that it is possible to both win and lose.</li>

</ol>

<h2>Code</h2>

Your code will be evaluated as follows. Each will be evaluated on a 0 to 5 basis, where 0 is unacceptable or not present, and 5 is excellent.

<h3>Functionality</h3>

Your program behaves as specified.

<h3>Direct Memory Access</h3>

You have implemented all LED interaction as specified

<h3>Watchdog</h3>

The watchdog works as specified.

<h3>Proper use of Registers, the stack, and link register</h3>

Only necessary items (no more, no less) are pushed onto the stack. Your function calls use the link register appropriately.

<h3>Code Readability and Structure</h3>

Your code is properly indented, does not wrap or have long lines, and can be logically understood.

You use subroutines and memory appropriately.

<h3>Code comments</h3>

As this is assembly language, you must extensively comment any code that is unclear (i.e. nearly every line).

<h2>Document Requirements</h2>

This assignment requires a single flowchart of the flow of your code. This flowchart should use standard flowchart shapes for steps and decisions, and should correspond with your logic.

Please print the table below, with your name clearly displayed, for marking purposes.

<table>

 <tbody>

  <tr>

   <td width="312">Item</td>

   <td width="312">Grade</td>

  </tr>

  <tr>

   <td width="312">Demonstration </td>

   <td width="312">/ 5</td>

  </tr>

  <tr>

   <td width="312">Code</td>

   <td width="312"></td>

  </tr>

  <tr>

   <td width="312">Functionality</td>

   <td width="312">/ 5</td>

  </tr>

  <tr>

   <td width="312">Direct Memory Access</td>

   <td width="312">/ 5</td>

  </tr>

  <tr>

   <td width="312">Watchdog</td>

   <td width="312">/ 5</td>

  </tr>

  <tr>

   <td width="312">Proper use of registers, etc.</td>

   <td width="312">/ 5</td>

  </tr>

  <tr>

   <td width="312">Readability</td>

   <td width="312">/ 5</td>

  </tr>

  <tr>

   <td width="312">Comments</td>

   <td width="312">/ 5</td>

  </tr>

  <tr>

   <td width="312">Code Subtotal </td>

   <td width="312">/ 35</td>

  </tr>

  <tr>

   <td width="312">Total </td>

   <td width="312">/ 35</td>

  </tr>

  <tr>

   <td width="312">Applicable Cap:</td>

   <td width="312"></td>

  </tr>

 </tbody>

</table>

<h3>Caps</h3>