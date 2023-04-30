Download Link: https://assignmentchef.com/product/solved-cs235-project-4-recursive-invert
<br>
For this project you will modify a <strong><u>singly-linked list</u></strong> class (<u>note</u> this is different from the doubly-linked list of Project 3) by adding a method that will invert the order of the list. This method <strong>must be recursive</strong> and should not involve loops.

<strong>GitHub Classroom assignment link: </strong><strong>https://classroom.github.com/a/lpskgJbK</strong>

<strong>The idea: </strong>In a linked list it is possible to invert the order of its elements in <strong>O(n) time</strong> and <strong>in place (O(1) extra space) </strong>simply by changing the direction of the links:

head_ptr

head_ptr

To do so recursively, you can think of the solution to the problem as:

<ul>

 <li><strong>Split the list into first and rest</strong></li>

 <li><strong>Reconnect rest to first in the appropriate direction</strong></li>

</ul>

head_ptr

<strong>Implementation: </strong>

In order to practice safe programming and not expose the structure of the list to clients of the class via pointer parameters, you will write a <strong><u>public</u></strong> <strong>non-recursive method</strong> <strong>invert</strong> that calls a <strong><u>private</u></strong> <strong>recursive</strong> <strong>method</strong> <strong>invertRest</strong>.

<strong>You must implement these methods in</strong> <strong>O(n) time</strong> and <strong>in place (you cannot use any additional list or other containers and cannot make copies of the nodes</strong>) Should you write a solution that uses iteration instead of recursion and /or uses additional containers or copies to invert the list, I reserve the right to take away points even if Gradescope gives you full credit.

// A  wrapper to a recursive method that inverts the contents of the list

// @post the contents of the list are inverted such that

//      the item previously at position 0 is at position item_count_-1, //      the item previously at position 1 is at position item_count_-2 …

//      the item previously at position ⌊item_count/2⌋ is at position

⌈item_count_/2⌉ . . .

//      the item previously at position item_count_-1 is at position 0 void invert();

//private function to invert, used for safe programming to avoid

//exposing pointers to list in public methods

// @post the contents of the list are inverted such that

//      the item previously at position 0 is at position item_count_-1, //      the item previously at position 1 is at position item_count_-2 …

//      the item previously at position ⌊item_count/2⌋ is at position

⌈item_count_/2⌉. . .

//     the item previously at position item_count_-1 is at position 0 void invertRest(Node&lt;T&gt;* current_first_ptr);

<strong>Testing:   </strong>

In main() (not for submission) instantiate a LinkedList object and add data (nodes) to it. The list could be of any type and it should not affect execution. Once you have data in the list, call invert and make sure it works correctly (e.g. display the contents of the list to check that the order is the opposite in which you inserted the data items).

Also test that your methods run correctly on edge cases (e.g. empty list, single-node list).

<strong>Notes:</strong><strong>  </strong>

<ul>

 <li>I reserve the right to detract points given by Gradescope if your submission does not comply in some way with this specification.</li>

 <li>A submission that implements all required classes and/or functions but <u>does not</u> <u>compile</u> will receive <u>40 points total (including documentation and design)</u>.</li>

</ul>