# NP HTML5, CSS3, and JavaScript 6e Tutorial 12, Case Problem 2

## instructions:
1.  Use your editor to open the sub_menu_txt.html and sub_cart_txt.js files from the html12 > case2 folder. Enter your name and the date in the comment section of each file, and save them as sub_menu.html and sub_cart.js respectively.
2.  Go to the sub_menu.html file in your editor. Add a script element to the document head for the sub_cart.js file, loading it asynchronously. Take some time to study the contents and structure of the file and then save your changes.
3.  Return to the sub_cart.js file in your editor. Add an event listener that runs the setupCart() func¬tion when the page is loaded.
4.  Create the setupCart() function. The purpose of this function is to define the event handlers for the Add to Order buttons on the page. Add the following commands to the function:
    a.  Create a variable named addButtons, which contains the collection of elements belonging to the addButton class.
    b.  Loop through the addButtons collection and for each button, add an event handler that runs the addItem() function when the button is clicked.
5.  Create the addltem() function, which adds items to the shopping cart on the page. Add the fol lowing commands to the function:
    a.  The description of the food item is the next sibling element to the button that was clicked by the customer. Use the nextElementSibling property to reference the next sibling element to the target of the event object. Store the sibling element in the variable foodltem.
    b.  Create the foodlD variable, which contains the value of the id attribute for foodItem.
    c.  Use the cloneNode() method to create a copy of the foodItem element and all of its descendants. Store this node structure in the foodDescription variable.
    d.  The shopping cart is stored in an aside element with the ID "cart". Store the reference to thiselement in a variable named cartBox. The shopping cart needs to determine whether a product ordered by the customer has already been ordered. To do this, you will add a span element to the top of each item in the cart con¬taining the number of items of each product ordered and update that value when a product order is repeated. Do the following to create the order counter for each Subsistence product.
    e.  Create a variable named duplicateOrder and set its initial value to false.
    f.  Loop through the element child nodes of cartBox. For each node, determine whether the ID of the element node equals foodID. If it does, the customer has previously placed that menu item in the cart. Increase the value of the first element child of node by 1 to indicate an additional order and then break out of the for loop.
    g.  After the for loop has completed, test whether duplicateOrder is still false. If it is, then cre-ate a variable named orderCount storing a span element node. Set the text content of the orderCount element to 1. Insert orderCount as the first child of the foodDescription node structure and append foodDescription to cartBox as a new product order.
6.  Document your work with comments throughout the JavaScript file and then save your work.
7.  Open sub_menu.html in your browser. Verify that when you click an Add to Order button, the description and image of the product is added to the shopping cart. Further verify that when you click the same food product several times, a running total of the number of items ordered is dis¬played in the shopping cart.
