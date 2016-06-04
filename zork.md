<!--djw: done -->
###Zork

#### Note: This is an advanced problem suitable for pairs, groups or talented individual students.

Zork was an early interactive computer game. It was initially released in 1977.


According to Wikipedia: 
<blockquote>Zork is set in "the ruins of an ancient empire lying far underground". The player is a nameless adventurer "who is venturing into this dangerous land in search of wealth and adventure". The goal is to return from exploring the "Great Underground Empire" (GUE, for short) alive and with all treasures needed to complete each adventure,[6] ultimately inheriting the title of Dungeon Master.
</blockquote>

We're not going to do all that. But in the spirit of Zork (and adventure) write an application that asks people what direction they wish to travel in. Once they tell you the direction, move them to the next room and tell them what is in it and what direction the other exits are.

Your setting will be a seven room haunted house. Good luck!

<table style="height: 226px;" border="1" width="384" cellspacing="1">
<tbody>
<tr>
<td></td>
<td>room</td>
<td>contains</td>
<td>doors to (direction &amp; room #)</td>
</tr>
<tr>
<td>#1</td>
<td>foyer</td>
<td>dead scorpion</td>
<td>room n2</td>
</tr>
<tr>
<td>#2</td>
<td>front room</td>
<td>piano</td>
<td>rooms s1,w3, e4</td>
</tr>
<tr>
<td>#3</td>
<td>library</td>
<td>spiders</td>
<td>rooms e2 &amp; n5</td>
</tr>
<tr>
<td>#4</td>
<td>kitchen</td>
<td>bats</td>
<td>rooms w2 &amp; n7</td>
</tr>
<tr>
<td>#5</td>
<td>
<p>dining room</p>
</td>
<td>
<p>dust</p>
<p>empty box</p>
</td>
<td>room s3</td>
</tr>
<tr>
<td>#6</td>
<td>vault</td>
<td>3 walking skeletons</td>
<td>room e7</td>
</tr>
<tr>
<td>#7</td>
<td>parlor</td>
<td>treasure chest</td>
<td>rooms w6, s4</td>
</tr>
</tbody>
</table>

Here's what your version of Zork will look like at the console:
```
You are standing in the front room of an old house.
You see a dead scorpion.
You can (1)exit to the east, (2) exit to the west.
1

You are standing in a library.
You see spiders.
You can (1) exit to the north, (2) exit to the east.
```
<!--
map:

| 5. Dining Room | 6. Valut | 7. Parlor |
| 3. Library     | 2. Piano | 4. Kitchen |
                 | 1. Foyer |
                 
enchancments:
add rooms
secret room (8) is only visible 25% of the time but once discovered stays visible
keep score - how many rooms have they visited
add javadoc comments
add list of fates
add list of items in room
timer if you take too long
treasure chest select treasure from random list

-->