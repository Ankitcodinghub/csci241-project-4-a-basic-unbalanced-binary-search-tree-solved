# csci241-project-4-a-basic-unbalanced-binary-search-tree-solved
**TO GET THIS SOLUTION VISIT:** [CSCI241 Project 4-A basic unbalanced binary search tree Solved](https://www.ankitcodinghub.com/product/csci241-data-structures-project-4-its-just-a-jump-to-the-left-and-a-step-to-the-right-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;120813&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;3&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (3 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CSCI241  Project 4-A basic unbalanced binary search tree Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

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
            5/5 - (3 votes)    </div>
    </div>
In this project, you will implement a basic unbalanced binary search tree and then add balance features to obtain optimal height.

<h1>Part I – Unbalanced Tree</h1>
Your primary focus in this part is recursion. Conceptually, binary search trees are fairly simple structures, so let’s take advantage of this implementation to develop our recursion skills. Review the recursive algorithm description in the BST slide deck very carefully. The wording is deliberate, and your implementation must follow the presented algorithms. We also suggest reviewing the associated videos to ensure that you understand the concepts before beginning your implementation.

When considering the traversal methods (which must also be recursive), remember that recursion works by dividing the problem into smaller components, then combining the smaller results to form the larger solution during the return path. Strings can be concatenated together to form larger strings using the + operator. Review the traversal algorithms and consider how the process of building the string can be divided into smaller steps and how those smaller strings can be combined to form the larger result. As one example, notice that the in-order traversal of a subtree rooted at node t is the concatenation of three strings: the in-order traversal of the subtree rooted at t’s left child, t’s value, and the in-order traversal of the subtree rooted at t’s right child.

Your implementation will also provide a get_height() method to obtain the number of levels in the tree. Note that this method is specified to operate in constant time. This means that height cannot be computed on demand, as counting the levels yields linear-time performance. Instead, add an attribute to the __Node class to store the height of the subtree rooted at that node. Just before returning a node reference at the end of a recursive call, update that node’s height field to be correct. If you do this before each return, then you know at all times that the height field of every node below you in the tree has the correct value. Because the heights of the subtrees rooted at t’s children are now known to be correct, we can say that t’s height is equal to the maximum of its children’s heights (accessible in constant time through child node attributes) plus 1. An important consideration here is that a non-existent subtree has height 0 (be careful not to crash in this case). Also notice that the height of the subtree rooted at a newly created node object is always 1.

In the example below, t’s height should be updated to 𝑟ℎ + 1 before it is returned. We choose 𝑟ℎ because the right subtree’s height is larger than the left subtree’s height. If every node in the tree stores the height of the subtree rooted at that node, then you can return the height of the entire tree in constant time.

&nbsp;

For one final reminder, notice that you cannot make the skeleton methods that we provide recursive. Because the only parameter that they take is the value being added or removed, and you cannot change the signatures of the public methods, you will have to introduce private accessory methods that are recursive. We did this in class. When asked to insert 50 into a BST, our public insert(50) method calls __recursive_insert(50, self.__root). That second parameter (t in my slides) is the recursion control variable that approaches the base case (t is the node representing the root of a smaller and smaller subtree until we hit a base case).

Additional details specific to each method including required exceptions are presented in the skeleton file.

<strong>Milestone Checkpoint:</strong> submit your unbalanced BST to gradescope for testing (this does not affect your grade, but it ensures that your tree construction is correct before you attempt balance operations.

<h1>Part II – AVL Balancing</h1>
In this part, you will extend your BST implementation in Binary_Search_Tree.py to guarantee 𝑂(log𝑛) insertions and removals. The changes required to support this are minimal. Provide a private method called __balance(t) that takes a node t as a parameter and treats it as the root of subtree. If the subtree rooted at t is unbalanced, rotate as necessary to balance it and return the new root of the now balanced subtree. Because this balance operation will be invoked on the return path from recursive insertion and removal, you can be sure that everything below t is already balanced. This means that checking to see if the tree rooted at t is balanced (and rotating it if it is not) is a constant time operation. You may also wish to introduce other additional private methods, as well.

If you followed the algorithms presented on the lecture slides and in class, all you have to do after writing the __balance(t) function is change the last line in your private recursive insert and remove methods from return t to return self.__balance(t) and reconsider when you compute height. Note that it is not necessary to check the balance of the new node created and returned in the base case, because it will always be balanced already. Be sure that when you return a subtree it is balanced and the height attribute of every node at or below t is correct (but only reevaluate the heights of nodes whose subtrees could potentially have changed—that is, every node on the insertion/removal path and every node actively involved in a rotation).

Once you have balanced insertions and removals implemented, implement the public/private method pair for recursively constructing a Python list of the values in the tree. This method should work just like the in-order traversal methods, but it should return a python list, not a string.

Finally, complete the implementation of the provided Fraction class by implementing the three comparison operators. The main section of this program should create a Python list of fraction objects, then insert them one at a time into an initially empty AVL tree, then get the in-order Python list representation using the new to_list method of Binary_Search_Tree, showing that the returned list is in sorted order.

&nbsp;

<h1>SUBMISSION EXPECTATIONS</h1>
<strong>Binary_Search_Tree.py</strong> This should be your implementation of an AVL tree. You are free to add additional private support methods (in fact, this is necessary), but do not change the public interface to this class.

<strong>BST_Test.py</strong> Your unit tests for implementations. No skeleton file is provided for this component. For testing, notice that the three traversals (in-order, post-order, and pre-order) uniquely identify a binary search tree. No two unequal trees share all three traversal orderings. Ensure that your traversals work correctly and use the combination of all three of them to test the structure of the tree after insertion and removal operations.

<strong>Fraction.py</strong> The provided Fraction class with the comparison methods implemented and with the main section sorting a Python list of fraction objects.
