# Inventory Management System

This project is a simple **Inventory Management System (IMS)** for a fictional magical shop, built using **JavaScript (ES6)**, **HTML**, and **CSS**. It allows users to add, remove, and manage inventory items while dynamically updating the interface.

* *Date Created*: 13 02 2025
* *Last Modification Date*: 13 02 2025
* *Project URL*: [https://web.cs.dal.ca/~mdmahajan/csci3172/labs/lab3/](https://web.cs.dal.ca/~mdmahajan/csci3172/labs/lab3/)
* *GitHub Repository*: [https://git.cs.dal.ca/mdmahajan/csci3172.git](https://git.cs.dal.ca/mdmahajan/csci3172.git)

## Authors

* **Malhar Mahajan** - Developer

## Built With

* [HTML5](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/HTML5) - Page structure
* [CSS3](https://developer.mozilla.org/en-US/docs/Web/CSS) - Styling and animations
* [JavaScript (ES6)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators) - Logic and interactivity
* [Git](https://git-scm.com/) - Version control

## Sources Used

### File: js/script.js

*Lines 18 - 36*

```javascript
function listItems() {
    const inventoryList = document.getElementById("inventory-list");
    inventoryList.innerHTML = "";
    
    inventory.forEach((item, index) => {
        let itemImage = item.image ? item.image : "img/unknown.jpg"; // Fallback to default if undefined

        inventoryList.innerHTML += `
            <div class="item-card">
                <img src="${itemImage}" alt="${item.name}" onerror="this.onerror=null; this.src='img/unkown.jpg';">
                <div class="item-details">
                    <strong>${item.name}</strong> (${item.type}) - $${item.price} | Stock: ${item.quantity} <br> ${item.description}
                </div>
                <button class="button-24" role="button" onclick="removeItem(${index})">Remove</button>
            </div>
        `;
    });
}

#   The code above was created by adapting the code in CSS SCAN for button animations and hover effects.

How: The code was implemented by replacing hardcoded item data with dynamic JavaScript, allowing inventory management.
Why: This code was used because it simplifies dynamically managing inventory.
How: The code was modified by adjusting the button styling for hover effects and adding conditional logic for item images.