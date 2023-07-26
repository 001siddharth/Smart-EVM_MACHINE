# Smart-EVM_MACHINE
**Approach Used** 
- We have stored the votes of each candidate in SR Latches and after the completion of 15 
sec from the first press of voters, the votes will be stored in the counter accumulating all the 
votes from different voters. At the end, you may press a push button to display the winner on 
7-Segment Display <br>
        **Features Added** <br>
  - Votes Comparator: The button named “Display Winner” when pressed compares the votes of all  
four candidates and prints ‘0’ if A wins, ‘1’ if B wins, ‘2’ if C wins, and ‘3’ if D wins. The 
comparator uses 3 four-bit comparator and 2 multiplexers
  - Display of Winner: The winner as output from comparator is shown on a 7-Segment Display for better 
readability on PCB. The Display will only function when the Display Winner button is 
pressed
  - MULTIPLE CANDIDATE VOTING: A voter may cast his vote(s) to any of the four candidates (one or more than one 
candidate) while only once for one candidate. The voter has a total time of 15 seconds in 
which he may cast his votes after which his votes will be registered
  - “Voted For” LEDs: Added four LEDs that display for which candidate the voter has voted. This feature 
removes any uncertainty in the minds of the voter that they might cast a wrong vote. A visual 
confirmation is the best way to remove any such confusion

![image](https://github.com/001siddharth/Smart-EVM_MACHINE/assets/98579609/bf129f16-48bd-4409-aa0c-1ef942a55b76)
  - REVERSE THE CASTED VOTE: As the votes are not registered into counters until 15 seconds have passed. The voter has this 15 seconds to alter his voting decisions. We have added four additional buttons to reverse a vote that voter may have casted mistakenly
    ![image](https://github.com/001siddharth/Smart-EVM_MACHINE/assets/98579609/6fa87724-9efa-403b-82f4-fd84db0c5b67)
  -  The ‘READY’ LED: As the votes are not registered into counters until 15 seconds have passed. The voter has this 15 seconds to alter his voting 
decisions. We have added four additional buttons to reverse a vote that voter may have cast mistakenly
  - 3 SECOND DELAY : 3-second delay is added after any button to cast a vote is pressed by the voter. 
This feature is to avoid any debouncing caused by the switch. However, as we are using SR 
Latch, which once set will not change its value until reset, overcomes this issue of 
debouncing without introducing any delay in the circuit.<br><br>
                                **PCB-layout**
<br><br>
Here as you can see in this PCB layout design we have generated the clock pulse of 
frequency 1Hz using N555 and with some resistors and capacitors. Each logic gate and 
IC’s VCC and GND terminal is connected with a connector with two inputs. Through pin
no.1 of the connector, we will supply VCC of 5V and Ground through pin no 2. Also, there 
is enable pin which will be activated by supplying 5V. And after enabling it will start 
comparing the votes of the candidates. And the result will be shown In the display attached.
We have done copper filling of Ground only because Filling a via with copper increases its 
thermal conductivity and higher conductivity will lead to high heat and may overheat the 
whole board and also may damage IC’s
![image](https://github.com/001siddharth/Smart-EVM_MACHINE/assets/98579609/8bb34fb6-576c-4b91-8c34-c3cf766dcccf)
<br> 
The Schematic of the Circuit <br>

![screenshot](https://github.com/001siddharth/Smart-EVM_MACHINE/assets/98579609/e663ed52-ccd1-4309-92c9-e5cf7d4a6014)

