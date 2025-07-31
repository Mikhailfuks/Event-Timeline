document.addEventListener('DOMContentLoaded', () => {
  const addButton = document.getElementById('add-button');
  const groceryList = document.getElementById('grocery-list');
  const groceryInput = document.getElementById('grocery-input');

  // Function to add a new grocery item
  const addGroceryItem = () => {
    const itemText = groceryInput.value.trim();
    if (itemText) {
      const listItem = document.createElement('li');
      listItem.textContent = itemText;

      const removeButton = document.createElement('button');
      removeButton.textContent = 'Remove';
      removeButton.classList.add('remove-button');
      removeButton.onclick = () => {
        groceryList.removeChild(listItem);
      };

      listItem.appendChild(removeButton);
      groceryList.appendChild(listItem);
      groceryInput.value = ''; // Clear the input field
    } else {
      alert('Please enter an item.');
    }
  };

  // Event listeners
  addButton.addEventListener('click', addGroceryItem);
  groceryInput.addEventListener('keypress', (event) => {
    if (event.key === 'Enter') {
      addGroceryItem();
    }
  });
});
//Run the code so that it works correctly

<!DOCTYPE html>
<html lang="en">

<head>
	<meta charset="UTF-8">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<title>Timeline</title>
	<link rel="stylesheet" href="styles.css">
</head>

<body>
	<h1>Event Timeline</h1>
	<div class="timeline" id="timeline"></div>
	<div id="details" class="details"></div>
	<script src="script.js"></script>
</body>

</html>

//Here is html code correctly 






script.css.disign



/* styles.css */
body {
    font-family: Arial, sans-serif;
    background-color: #f4f4f4;
    color: #333;
    text-align: center;
}

h1 {
    margin: 20px 0;
}

.timeline {
    position: relative;
    width: 50%;
    margin: 0 auto;
    padding: 20px 0;
}

.event {
    padding: 10px 20px;
    background-color: #007bff;
    color: white;
    margin: 10px 0;
    border-radius: 5px;
    cursor: pointer;
    transition: background 0.3s;
}

.event:hover {
    background-color: #0056b3;
}

.details {
    margin-top: 20px;
    padding: 15px;
    background-color: #fff;
    border-radius: 5px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
}

