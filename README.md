Download Link: https://assignmentchef.com/product/solved-database-systems-assignment-3-product
<br>
5/5 - (2 votes)

<table class="highlight tab-size js-file-line-container" data-tab-size="8">

 <tbody>

  <tr>

   <td id="L6" class="blob-num js-line-number" data-line-number="6"></td>

   <td id="LC6" class="blob-code blob-code-inner js-file-line">Reading: The posted Lecture 5 and Lecture 6 Slides, and Ullman/Widom Sections 6.1-6.2 and 6.4. [Next week: Ullman/Widom Sections 6.2-6.3.]</td>

  </tr>

  <tr>

   <td id="L7" class="blob-num js-line-number" data-line-number="7"></td>

   <td id="LC7" class="blob-code blob-code-inner js-file-line"></td>

  </tr>

  <tr>

   <td id="L8" class="blob-num js-line-number" data-line-number="8"></td>

   <td id="LC8" class="blob-code blob-code-inner js-file-line">Your task in this assignment is to write a set of SQL queries (I will supply the  tables).</td>

  </tr>

  <tr>

   <td id="L9" class="blob-num js-line-number" data-line-number="9"></td>

   <td id="LC9" class="blob-code blob-code-inner js-file-line"></td>

  </tr>

  <tr>

   <td id="L10" class="blob-num js-line-number" data-line-number="10"></td>

   <td id="LC10" class="blob-code blob-code-inner js-file-line">First, download the script file Furniture.sql from the dropbox and run it in SQLDeveloper to build the tables you will be querying.</td>

  </tr>

  <tr>

   <td id="L11" class="blob-num js-line-number" data-line-number="11"></td>

   <td id="LC11" class="blob-code blob-code-inner js-file-line"></td>

  </tr>

  <tr>

   <td id="L12" class="blob-num js-line-number" data-line-number="12"></td>

   <td id="LC12" class="blob-code blob-code-inner js-file-line">This script will build and display the contents of the following four tables that store data for a fictitious furniture supplier:</td>

  </tr>

  <tr>

   <td id="L13" class="blob-num js-line-number" data-line-number="13"></td>

   <td id="LC13" class="blob-code blob-code-inner js-file-line"></td>

  </tr>

  <tr>

   <td id="L14" class="blob-num js-line-number" data-line-number="14"></td>

   <td id="LC14" class="blob-code blob-code-inner js-file-line">CUSTOMER(CustomerID, Name, Address, City, State, Zip), which contains information on customers of the company;</td>

  </tr>

  <tr>

   <td id="L15" class="blob-num js-line-number" data-line-number="15"></td>

   <td id="LC15" class="blob-code blob-code-inner js-file-line"></td>

  </tr>

  <tr>

   <td id="L16" class="blob-num js-line-number" data-line-number="16"></td>

   <td id="LC16" class="blob-code blob-code-inner js-file-line">PRODUCT(ProductID, Description, Finish, Price), which contains information on products sold by the company;</td>

  </tr>

  <tr>

   <td id="L17" class="blob-num js-line-number" data-line-number="17"></td>

   <td id="LC17" class="blob-code blob-code-inner js-file-line"></td>

  </tr>

  <tr>

   <td id="L18" class="blob-num js-line-number" data-line-number="18"></td>

   <td id="LC18" class="blob-code blob-code-inner js-file-line">ORDERTABLE(OrderID, OrderDate, CustomerID), which contains information on orders placed with the company;</td>

  </tr>

  <tr>

   <td id="L19" class="blob-num js-line-number" data-line-number="19"></td>

   <td id="LC19" class="blob-code blob-code-inner js-file-line"></td>

  </tr>

  <tr>

   <td id="L20" class="blob-num js-line-number" data-line-number="20"></td>

   <td id="LC20" class="blob-code blob-code-inner js-file-line">ORDERLINE(OrderID, ProductID, Quantity), which contains information on the individual products requested in customers’ orders.</td>

  </tr>

  <tr>

   <td id="L21" class="blob-num js-line-number" data-line-number="21"></td>

   <td id="LC21" class="blob-code blob-code-inner js-file-line"></td>

  </tr>

  <tr>

   <td id="L22" class="blob-num js-line-number" data-line-number="22"></td>

   <td id="LC22" class="blob-code blob-code-inner js-file-line">In additional to the primary keys indicated above, OrderID and ProductID in ORDERLINE are foreign keys referencing OrderID in ORDERTABLE and ProductID in PRODUCT, respectively, and CustomerID in ORDERTABLE is a foreign key referencing CustomerID in CUSTOMER.</td>

  </tr>

  <tr>

   <td id="L23" class="blob-num js-line-number" data-line-number="23"></td>

   <td id="LC23" class="blob-code blob-code-inner js-file-line"></td>

  </tr>

  <tr>

   <td id="L24" class="blob-num js-line-number" data-line-number="24"></td>

   <td id="LC24" class="blob-code blob-code-inner js-file-line">In SQLDeveloper, look at the Columns, Data, and Constraints for each of the four tables before continuing, to be sure that they have been constructed correctly. You might also want to draw the foreign keys and reference arrows into the set of relation schemas given above to be sure that you understand the links among the tables.</td>

  </tr>

  <tr>

   <td id="L25" class="blob-num js-line-number" data-line-number="25"></td>

   <td id="LC25" class="blob-code blob-code-inner js-file-line"></td>

  </tr>

  <tr>

   <td id="L26" class="blob-num js-line-number" data-line-number="26"></td>

   <td id="LC26" class="blob-code blob-code-inner js-file-line">For each of the following query problems, follow the steps we discussed in class: interpret the problem, predict the output by solving it by hand on the table in question, write a query to solve the problem, and test the query. (Most of the query problems can be solved with information from just one of the given tables, but some will require joins.)</td>

  </tr>

  <tr>

   <td id="L27" class="blob-num js-line-number" data-line-number="27"></td>

   <td id="LC27" class="blob-code blob-code-inner js-file-line"></td>

  </tr>

  <tr>

   <td id="L28" class="blob-num js-line-number" data-line-number="28"></td>

   <td id="LC28" class="blob-code blob-code-inner js-file-line">For each query, when you have it working correctly, include in your submission document a single screen shot that shows your open SQLDeveloper connection, the query displayed in the center window, and the entire result of the query in the Query Result window. (You may have to resize the Query Result window to see the entire result.) Be sure that the query and result are big enough to be readable. Also include the query number in your document before each screenshot.</td>

  </tr>

  <tr>

   <td id="L29" class="blob-num js-line-number" data-line-number="29"></td>

   <td id="LC29" class="blob-code blob-code-inner js-file-line"></td>

  </tr>

  <tr>

   <td id="L30" class="blob-num js-line-number" data-line-number="30"></td>

   <td id="LC30" class="blob-code blob-code-inner js-file-line"></td>

  </tr>

  <tr>

   <td id="L31" class="blob-num js-line-number" data-line-number="31"></td>

   <td id="LC31" class="blob-code blob-code-inner js-file-line">1. Give an alphabetical list of all states that have at least one customer.</td>

  </tr>

  <tr>

   <td id="L32" class="blob-num js-line-number" data-line-number="32"></td>

   <td id="LC32" class="blob-code blob-code-inner js-file-line"></td>

  </tr>

  <tr>

   <td id="L33" class="blob-num js-line-number" data-line-number="33"></td>

   <td id="LC33" class="blob-code blob-code-inner js-file-line">2. Give all of the information for customers in California, alphabetized by customer name.</td>

  </tr>

  <tr>

   <td id="L34" class="blob-num js-line-number" data-line-number="34"></td>

   <td id="LC34" class="blob-code blob-code-inner js-file-line"></td>

  </tr>

  <tr>

   <td id="L35" class="blob-num js-line-number" data-line-number="35"></td>

   <td id="LC35" class="blob-code blob-code-inner js-file-line">3. For each customer who has placed at least one order, give the customer’s ID and the date of their earliest order. Sort the output by the customers’ IDs.</td>

  </tr>

  <tr>

   <td id="L36" class="blob-num js-line-number" data-line-number="36"></td>

   <td id="LC36" class="blob-code blob-code-inner js-file-line"></td>

  </tr>

  <tr>

   <td id="L37" class="blob-num js-line-number" data-line-number="37"></td>

   <td id="LC37" class="blob-code blob-code-inner js-file-line">4. Give the state and zip for all customers in New York and California.</td>

  </tr>

  <tr>

   <td id="L38" class="blob-num js-line-number" data-line-number="38"></td>

   <td id="LC38" class="blob-code blob-code-inner js-file-line"></td>

  </tr>

  <tr>

   <td id="L39" class="blob-num js-line-number" data-line-number="39"></td>

   <td id="LC39" class="blob-code blob-code-inner js-file-line">5. Give the finish and description of each product, sorted alphabetically by finish, and with the products with each finish given in order from the one with the highest price to the one with the lowest price.</td>

  </tr>

  <tr>

   <td id="L40" class="blob-num js-line-number" data-line-number="40"></td>

   <td id="LC40" class="blob-code blob-code-inner js-file-line"></td>

  </tr>

  <tr>

   <td id="L41" class="blob-num js-line-number" data-line-number="41"></td>

   <td id="LC41" class="blob-code blob-code-inner js-file-line">6. Give the names of all customers with the word ‘Furnishings’ somewhere in their name.</td>

  </tr>

  <tr>

   <td id="L42" class="blob-num js-line-number" data-line-number="42"></td>

   <td id="LC42" class="blob-code blob-code-inner js-file-line"></td>

  </tr>

  <tr>

   <td id="L43" class="blob-num js-line-number" data-line-number="43"></td>

   <td id="LC43" class="blob-code blob-code-inner js-file-line">7. For each date on which at least one order has been placed, give the date and the number of orders placed on that date. Sort the output by the date.</td>

  </tr>

  <tr>

   <td id="L44" class="blob-num js-line-number" data-line-number="44"></td>

   <td id="LC44" class="blob-code blob-code-inner js-file-line"></td>

  </tr>

  <tr>

   <td id="L45" class="blob-num js-line-number" data-line-number="45"></td>

   <td id="LC45" class="blob-code blob-code-inner js-file-line">8. For each order, give the order ID and the total number of items requested in that order (e.g., for an order that requested 4 of one product, 3 of a second product, and 1 of a third product, the total number of items reported for that order should be 8). Sort the orders from the one with the smallest number of items to the one with the largest.</td>

  </tr>

  <tr>

   <td id="L46" class="blob-num js-line-number" data-line-number="46"></td>

   <td id="LC46" class="blob-code blob-code-inner js-file-line"></td>

  </tr>

  <tr>

   <td id="L47" class="blob-num js-line-number" data-line-number="47"></td>

   <td id="LC47" class="blob-code blob-code-inner js-file-line">9. For each order, give the order ID and the city and state of the customer who placed that order. Sort the output by the order ID.</td>

  </tr>

  <tr>

   <td id="L48" class="blob-num js-line-number" data-line-number="48"></td>

   <td id="LC48" class="blob-code blob-code-inner js-file-line"></td>

  </tr>

  <tr>

   <td id="L49" class="blob-num js-line-number" data-line-number="49"></td>

   <td id="LC49" class="blob-code blob-code-inner js-file-line">10. For each product, give the product name and a count of how many orders have requested it. (Don’t worry about the quantity of the product requested by each order, just count the number of order that requested any amount of the product.) Order the output by the product ID.</td>

  </tr>

  <tr>

   <td id="L50" class="blob-num js-line-number" data-line-number="50"></td>

   <td id="LC50" class="blob-code blob-code-inner js-file-line"></td>

  </tr>

 </tbody>

</table>