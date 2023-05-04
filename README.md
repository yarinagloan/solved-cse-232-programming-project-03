Download Link: https://assignmentchef.com/product/solved-cse-232-programming-project-03
<br>
<h2>Assignment Overview</h2>

This assignment will give you more experience on the use of loops and conditionals, and introduce the use of functions.




<h2>Background</h2>

Games have been interesting to computer scientists for, well since there was computer science. Not shoot-em-up, blood-and-gore games, those are just silly. We are talking about games that can be analyzed and their properties understood. In so doing we can design algorithms that do a better job solving a game, and perhaps apply those algorithms to other problems.




Anyway, let’s play the game rock-papers-scissors.




<h2>Rock-Paper-Scissors</h2>

Let’s call it RPS, I am a CS person afterall. RPS is a children’s game, a two player game that involves the two players choosing one of three hand gestures to see who wins a round of play, see <u>https://en.wikipedia.org/wiki/Rock-paper-scissors</u> . If you read the link to associated Ken games, <u>https://en.wikipedia.org/wiki/Sansukumi-ken</u>, you would see that it’s origins are less than child-like. It seems to have started as a game from Asia (in China, in Japan), one of a series of such games, that had to do with brothel’s and drinking games. How quaint!




<h2>The Rules</h2>

The rules are pretty simple, as illustrated by the Wikipedia page image shown below.







In this two-player game, each player can make one of three hand gestures. The players simultaneously (usually after the count of three) show their hand gesture and determine a winner. One of two outcomes is possible:

<ul>

 <li>both players select the same hand gesture, resulting in a tie.</li>

 <li>one player wins the round. The rules as shown are:</li>

</ul>

o rock wins over scissors o scissors wins over paper o paper wins over rock <strong>Project Description / Specification </strong>




<h2>Input and Output</h2>

We are going to use integers here to mean different things in different contexts so pay attention: • The legal player numbers are 1 or 2 (player1 or player2)

<ul>

 <li>For game moves: 1 is rock, 2 is paper, 3 is scissors.</li>

 <li>For scoring purposes: 0 is a tie, 1 means player1 won, 2 means player2 won.</li>

</ul>




<h2>main</h2>

We are going to write some strategies to play RPS, and then run those strategies to see how they fare.  We provide a skeleton file to start with that contains a predefined main. You can begin by editing this file and filling in the functions in the provided space. This updated file, with the unchanged predefined main, is what you will turn into Mimir<strong>. Do not change the main program</strong>! It will mess with the tests and you won’t get the credit you deserve! The TAs will check for this during grading. All you do is provide the required functions.




The main program uses a switch statement to determine which functions to run. The first argument to main is the switch input value. Subsequent input values depend on the input needs for the function selected.




We will provide you with <strong>some starter code</strong> that has the main function written without the functions that you can fill in.




<h2>Functions</h2>

The 3 functions take the same arguments, even if that particular strategy doesn’t need to use the information in all the arguments. Makes calling the functions more standard.




<strong>function</strong>: strategy1:

<ul>

 <li>return is int, the move rock(1), paper(2) or scissors(3) you select for the next round.</li>

 <li>Arguments are four integers in the following order:

  <ul>

   <li>player : which player are you (1 or 2).</li>

   <li>previous_result : 0 if a tie otherwise 1 or 2 indicating player1 or player2 won the last round.</li>

   <li>previous_play: 1, 2 or 3 if this player (the player of the first argument) played rock(1), paper(2) or scissors(3) in the last round.</li>

   <li>opponent_previous_play: 1, 2 or 3 if the <strong>other</strong> player played rock(1), paper(2) or scissors(3) in the last round.</li>

  </ul></li>

</ul>

This function represents a simple strategy. It cycles through rock(1), paper(2) or scissors(3) in that exact order. Thus if your previous_play was: 1 you return 2; if 2 returns 3; if 3 returns 1;




<strong>function</strong>: strategy2:

<ul>

 <li>return is int, the move rock(1), paper(2) or scissors(3) you select for the next round.</li>

 <li>Arguments are four integers in the following order:

  <ul>

   <li>player : which player are you (1 or 2).</li>

   <li>previous_result : 0 if a tie otherwise 1 or 2 indicating player1 or player2 won the last round.</li>

   <li>previous_play: 1,2 or 3 if this player played rock(1), paper(2) or scissors(3) in the last round.</li>

   <li>opponent_previous_play: 1,2 or 3 if the other player played rock(1), paper(2) or scissors(3) in the last round.</li>

  </ul></li>

</ul>

This is the stick-or-switch strategy. If you <strong>won or tied</strong> the last round return your previous play. Otherwise, return your opponent’s previous play.




<strong>function</strong>: strategy3:

<ul>

 <li>return is int, the move rock(1), paper(2) or scissors(3) you select for the next round.</li>

 <li>Arguments are four integers in the following order:

  <ul>

   <li>player : which player are you (1 or 2).</li>

   <li>previous_result : 0 if a tie otherwise 1 or 2 indicating player1 or player2 won the last round. o previous_play: 1,2 or 3 if this player played rock(1), paper(2) or scissors(3) in the last round.</li>

   <li>opponent_previous_play: 1,2 or 3 if the other player played rock(1), paper(2) or scissors(3) in the last round.</li>

  </ul></li>

</ul>

This is the stick-or-win strategy. If you <strong>won or tied</strong> the last round, return your previous play. Otherwise, return a move that would <strong>beat</strong> your opponent’s previous play.




<strong>function</strong>: score_round:

<ul>

 <li>return is int. 0 for tie, otherwise 1 or 2 (which player won player1(1) or player2(2) ).</li>

 <li>Arguments are two integers:

  <ul>

   <li>player1 move and player2 move (in that order). Each has a value of rock(1), paper(2) or scissors(3), the play made by each player.</li>

  </ul></li>

</ul>

Which player (1 or 2) won this round, or a 0 if it was a tie.

<strong> </strong>


