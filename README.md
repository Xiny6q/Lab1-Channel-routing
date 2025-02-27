Download link :https://programming.engineering/product/lab1-channel-routing/


# Lab1-Channel-routing
Lab1 – Channel routing
Problem description

Implement a 2-layer detailed router to complete channel routing problems. You need to use the greedy channel routing algorithm.

Input/Output Format

Input:

The input file consists of two rows of integers, where each number represents the net id of the pin except for 0. All the pins located at the top and bottom rows with the same net id must be connected together.

Example:

0 1 3 2 11 5 3 1 0



1 5 11 5 1 1 4 2 4

Output:

Print out all horizontal and vertical segments of every net in a file. The column’s width and track’s height are 1. The coordinate of the bottom layer starts from 0.

Format:

.begin net_name

.H lef_x lef_y rig_x

.V bot_x bot_y top_y

.end



Example. The above figure displays the routing of net 4 (three pins and 5 vias).

.begin 4

.H012

.V001

.V101

.V212

.H223

.V323

.end


Note that. There is no fixed wire segment order. A via is induced by the intersection of one horizontal and one vertical wire segment of the same net, and we set via cost = 5. If two wire segments of different nets with the same direction overlap, a short error occurs. You can use the verifier to examine the routing

errors. Besides, please notice that the top and bottom rows can’t place any horizontal wire segments (for example, “.H 0 0 1” is illegal in the above case).

Appendix

Verfier.

We provide a verifier to check the correctness of your program.

./verifier [output.txt] [input.txt]

If the terminal shows “All signals are connected successfully. “, it means your program passes the verifier. Then it will also show your track count and total wire length(including via cost), which are the basis of our grading.

Plotter.

We provide a Python plotter that can help you debug from the visualized routing result.

python plotter.py –in_file input_filename –out_file output_filename — img_name img_name

You can execute the following command to see an example result of case1

python plotter.py –in_file testbench/case1.txt –out_file result.txt –img_name example



Notice that. The final grade is based on the output message of the verifier, the Python plot is only for reference.

Makefile.

We also provide a Makefile to help you build your code. You can also write your own Makefile as long as it can be executed by the “make” command and generate a

specified executable.

Executing Procedure

We’ll use “make” command to build your code, please make sure that your Makefile can generate an executable named Lab1

2. ./Lab1 [input.txt] [output.txt]

Search for [output.txt], if not found→ break → 0 point

./ verifier [output.txt] [input.txt]

If fail → break→ 0 point

Submission

Please submit the following materials in a .zip file to E3 by the deadline, specifying your student ID in the subject field (e.g., StudentID.zip):

Source codes (.cpp, .h …)

Makefile

Grade

Notice that we provide several testcases, but your score is evaluated only based on the output result of testcase “Deutsch_difficult.txt”, and the grading rule is listed below:

For each case, the runtime limit is up to 300 seconds. It will be regarded as

“failed” if you use more than 300 seconds.

Spill-over area is allowed, but you will get an additional penalty according to the width of spill-over region.

penalty = -(the width of spill-over region)

Ranking is categorized into the following sets according to your track number of “Deutsch_difficult.txt”. You’ll get 100 if your track number is 19. Notice that if two or more students have the same track number (except 19), we’ll compare your wire length to determine who will get a higher score.

Maximum tracks

Minimum tracks

Score region

infinity

53

[70, 75)

53

44

[75-80)

43

34

[80-85)

33

28

[85-90)

27

25

[90-95)

24

20

[95-100)

19

100

Suppose your program can generate a correct routing result of

“Deutsch_difficult.txt” in 300 seconds, and there are students in the

same score region , then your score should be

Score = min⁡(r)⁡+ max⁡(0, 5 × +1− _ _ _ ℎ _ _ + penalty)

Late submission: Score * 8 before 4/3. After 4/3, you will get 0 point

Wrong submission format: 10 points punishment

Any work by fraud will absolutely get 0 point

Problem description

Implement a 2-layer detailed router to complete channel routing problems. You need to use the greedy channel routing algorithm.

Input/Output Format

Input:

The input file consists of two rows of integers, where each number represents the net id of the pin except for 0. All the pins located at the top and bottom rows with the same net id must be connected together.

Example:

0 1 3 2 11 5 3 1 0



1 5 11 5 1 1 4 2 4

Output:

Print out all horizontal and vertical segments of every net in a file. The column’s width and track’s height are 1. The coordinate of the bottom layer starts from 0.

Format:

.begin net_name

.H lef_x lef_y rig_x

.V bot_x bot_y top_y

.end



Example. The above figure displays the routing of net 4 (three pins and 5 vias).

.begin 4

.H012

.V001

.V101

.V212

.H223

.V323

.end


Note that. There is no fixed wire segment order. A via is induced by the intersection of one horizontal and one vertical wire segment of the same net, and we set via cost = 5. If two wire segments of different nets with the same direction overlap, a short error occurs. You can use the verifier to examine the routing

errors. Besides, please notice that the top and bottom rows can’t place any horizontal wire segments (for example, “.H 0 0 1” is illegal in the above case).

Appendix

Verfier.

We provide a verifier to check the correctness of your program.

./verifier [output.txt] [input.txt]

If the terminal shows “All signals are connected successfully. “, it means your program passes the verifier. Then it will also show your track count and total wire length(including via cost), which are the basis of our grading.

Plotter.

We provide a Python plotter that can help you debug from the visualized routing result.

python plotter.py –in_file input_filename –out_file output_filename — img_name img_name

You can execute the following command to see an example result of case1

python plotter.py –in_file testbench/case1.txt –out_file result.txt –img_name example



Notice that. The final grade is based on the output message of the verifier, the Python plot is only for reference.

Makefile.

We also provide a Makefile to help you build your code. You can also write your own Makefile as long as it can be executed by the “make” command and generate a

specified executable.

Executing Procedure

We’ll use “make” command to build your code, please make sure that your Makefile can generate an executable named Lab1

2. ./Lab1 [input.txt] [output.txt]

Search for [output.txt], if not found→ break → 0 point

./ verifier [output.txt] [input.txt]

If fail → break→ 0 point

Submission

Please submit the following materials in a .zip file to E3 by the deadline, specifying your student ID in the subject field (e.g., StudentID.zip):

Source codes (.cpp, .h …)

Makefile

Grade

Notice that we provide several testcases, but your score is evaluated only based on the output result of testcase “Deutsch_difficult.txt”, and the grading rule is listed below:

For each case, the runtime limit is up to 300 seconds. It will be regarded as

“failed” if you use more than 300 seconds.

Spill-over area is allowed, but you will get an additional penalty according to the width of spill-over region.

penalty = -(the width of spill-over region)

Ranking is categorized into the following sets according to your track number of “Deutsch_difficult.txt”. You’ll get 100 if your track number is 19. Notice that if two or more students have the same track number (except 19), we’ll compare your wire length to determine who will get a higher score.

Maximum tracks

Minimum tracks

Score region

infinity

53

[70, 75)

53

44

[75-80)

43

34

[80-85)

33

28

[85-90)

27

25

[90-95)

24

20

[95-100)

19

100

Suppose your program can generate a correct routing result of

“Deutsch_difficult.txt” in 300 seconds, and there are students in the

same score region , then your score should be

Score = min⁡(r)⁡+ max⁡(0, 5 × +1− _ _ _ ℎ _ _ + penalty)

Late submission: Score * 8 before 4/3. After 4/3, you will get 0 point

Wrong submission format: 10 points punishment

Any work by fraud will absolutely get 0 point

