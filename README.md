Download Link: https://assignmentchef.com/product/solved-cs577-homework3
<br>
<h1></h1>

<ol>

 <li> Suppose you are given a string of letters representing text in some foreign language, but without any spaces or punctuation. You want to break this string into its individual constituent words. For example, you might be given the following passage from Cicero’s famous oration in defense of Lucius Licinius Mureta in 62bce, in the <em>scriptia continua </em>of classical Latin:</li>

</ol>

PRIMVSDIGNITASINTAMTENVISCIENTIANONPOTEST

ESSERESENIMSVNTPARVAEPROPEINSINGVLISLITTERIS

ATQVEINTERPVNCTIONIBUSVERBORVMOCCVPATAE<a href="#_ftn1" name="_ftnref1"><sup>[1]</sup></a>

A fluent Latin reader would parse this string (in modern orthography) as <em>Primus dignitas in tam tenui scientia non potest esse; res enim sunt parvae, prope in singulis litteris atque interpunctionibus verborum occupatae</em>.

Some strings can be parsed in multiple ways, but you are not concerned with that. You want to know, given a string <em>S </em>of <em>n </em>characters, can it be segmented into words <em>at all</em>? Assume you have access to a subroutine IsWord(<em>i,j</em>) that takes indices <em>i,j </em>with <em>i </em>≤ <em>j </em>as input and indicates whether <em>S</em>[<em>i,…,j</em>] is a “word” in the foreign language, and that it takes constant time to run.

Design an algorithm that solves this problem in <em>O</em>(<em>n</em><sup>2</sup>) time.

<ol start="2">

 <li>Recall that a subsequence of an array is obtained by deleting any number of positions (possibly none, possibly all). A subarray is a sequence in which the positions that are not deleted form an interval (possibly empty). For example, consider the array [−1<em>,</em>−2<em>,</em>−3<em>,</em>−4<em>,</em>−5]. A valid subsequence is [−1<em>,</em>−3<em>,</em>−5]; it is not a subarray. A valid subarray is [−2<em>,</em>−3].</li>

</ol>

You are given an array <em>A</em>[1<em>,…,n</em>] of integers and want to find the maximum sum of the elements of (a) any subsequence, and (b) any subarray. The sum of an empty subarray is 0. For the example above, the maximum-sum subarray and subsequence has length zero.

Design an <em>O</em>(<em>n</em>) algorithm for both problems.

<h1>Regular problems</h1>

<ol start="3">

 <li>You want to go running and have <em>n </em>minutes to spare. You want to run as long a distance as possible, but your exhaustion level cannot exceed a given limit <em>e</em>. Initially your exhaustion level is zero. During each minute, you can choose to either run or rest for the whole minute. When you choose to run the <em>i</em>-th minute, you run exactly <em>d</em>[<em>i</em>] feet during that minute, and your exhaustion level increases by one. When you choose to rest, you run zero feet during that minute, and your exhaustion level decreases by one (if your exhaustion level is already zero, it will stay zero). Moreover, when you choose to rest, you must continue to rest until your exhaustion level reaches zero; once it reaches zero, you can again choose to run or rest. Finally, your exhaustion level at the end of your run must be zero.</li>

</ol>

For example, for <em>e </em>= 2 and <em>d</em>[1<em>,…,</em>5] = (500<em>,</em>300<em>,</em>400<em>,</em>200<em>,</em>1000), the best you can do is to run during minutes 1 and 3, and rest the other minutes, so the answer is 500 + 400 = 900.

Develop an algorithm that takes a positive integer <em>e </em>and an array <em>d</em>[1<em>,…,n</em>] of <em>n </em>≥ 1 positive integers as input, and ouputs the maximum distance you can run subject to the constraints above. Your algorithm should run in time <em>O</em>(<em>ne</em>) and space <em>O</em>(<em>e</em>).

<ol start="4">

 <li>When you were little, every day on your way home from school you passed the house of your grandmother. If you stop by for a chat on day <em>i</em>, Grandma would give you a number <em>`<sub>i </sub></em>of lollipops but also tell you that she won’t give you any more lollipops for the next <em>k<sub>i </sub></em> For example, if day 1 is a Monday and <em>k</em><sub>1 </sub>= 3, then if you visit her that day, you would have to wait patiently until Friday to get your next lollipop.</li>

</ol>

Design an <em>O</em>(<em>n</em>) algorithm that takes as input the numbers (<em>`<sub>i</sub>,k<sub>i</sub></em>) for <em>i </em>∈{1<em>,</em>2<em>,…,n</em>}, and outputs the maximum number of lollipops you can get during those <em>n </em>days.

<ol start="5">

 <li>The library has <em>n </em>books that must be stored in alphabetical order on adjustable-height shelves. Each book has a height, and a thickness. The width of the shelf is fixed at <em>w</em>, and the sum of the thicknesses of books on a single shelf cannot exceed <em>w</em>. The next shelf will be placed atop the tallest book on the shelf. You can assume the shelving takes no vertical space.</li>

</ol>

Design an algorithm that minimizes the total height of shelves used to store all the books. You are given the list of books in alphabetical order. Your algorithm should run in time <em>O</em>(<em>n</em><sup>2</sup>).

<h1>Challenge problem</h1>

<ol start="6">

 <li>There is a famous joke-riddle for children:</li>

</ol>

Three turtles are crawling along a road. One turtle says, “There are two turtles ahead of me.” Another turtle says, “There are two turtles behind me.” The third turtle says, “There are two turtles ahead of me and two turtles behind me.” How could this have happened? Of course, the third turtle is lying!

In this problem you have <em>n </em>turtles crawling along a road. Some of them are crawling sideby-side, so there may be turtles that are neither ahead nor behind one another. Each turtle makes a statement of the form: “There are <em>a<sub>i </sub></em>turtles ahead of me, and <em>b<sub>i </sub></em>turtles behind me.”

Your task is to find the minimal number of turtles that must be lying. More formally, let <em>x<sub>i </sub></em>denote the position along the road of turtle <em>i</em>, 1 ≤ <em>i </em>≤ <em>n</em>. Some turtles may be at the same position. Turtle <em>i </em>tells the truth if and only if <em>a<sub>i </sub></em>is the number of turtles <em>j </em>such that <em>x<sub>j </sub>&gt; x<sub>i </sub></em>and <em>b<sub>i </sub></em>is the number of turtles <em>j </em>such that <em>x<sub>j </sub>&lt; x<sub>i</sub></em>. Otherwise, turtle <em>i </em>is lying.

Design an <em>O</em>(<em>n</em>log<em>n</em>) algorithm for this problem.

<h1>Programming problem</h1>

<ol start="7">

 <li>SPOJ problem <a href="https://www.spoj.com/problems/MCOINS">Coins Game</a> (problem code MCOINS).</li>

</ol>

<a href="#_ftnref1" name="_ftn1">[1]</a> “First of all, dignity in such paltry knowledge is impossible; this is trivial stuff, mostly concerned with individual letters and the placement of points between words.”