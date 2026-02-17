Spots – Interactive Card Gallery
📌 Project Overview

Spots is a dynamic, interactive photo gallery built with HTML, CSS, and JavaScript.
The application demonstrates DOM manipulation, template cloning, event handling, and modal interactions.

This project was developed as part of the TripleTen Software Engineering program and focuses on dynamically generating UI components using JavaScript instead of hardcoded HTML.

🚀 Features Implemented
1️⃣ Dynamic Card Generation (Template-Based)

Cards are generated using a <template> element in HTML.

No hardcoded cards exist in the markup.

Cards are created dynamically from the initialCards array.

Each card includes:

Image

Title

Like button

Delete button

The getCardElement(data) function:

Clones the template

Assigns:

data.link → image src

data.name → image alt

data.name → title textContent

Adds event listeners for like, delete, and preview

Returns the completed card element

Cards are rendered using:

initialCards.forEach((item) => {
  const card = getCardElement(item);
  cardsContainer.prepend(card);
});

2️⃣ “New Post” Modal Submission

Users can create a new card using the “New Post” modal.

On form submission:

A new card is generated using getCardElement()

The card is prepended to the container

The modal closes automatically

Form fields are cleared

3️⃣ Like Button Functionality

Each card has a heart-shaped like button.

Clicking the button toggles a CSS class:

cardLikeButton.classList.toggle("card__like-btn_active");


The appearance changes dynamically via CSS.

4️⃣ Delete Button Functionality

Each card includes a trashcan-shaped delete button.

Clicking the delete button removes the card from the DOM:

cardElement.remove();

5️⃣ Preview Image Modal

Clicking on a card image opens a preview modal.

The modal displays:

A larger version of the image

The image caption

The modal:

Centers properly on all screen sizes

Uses max dimensions of 80vw and 80vh on desktop

Close functionality:

Close button

Overlay click

Escape key

🛠 Technologies Used

HTML5

CSS3 (Responsive Design)

JavaScript (ES6)

DOM Manipulation

Template Cloning

Event Handling

📂 Project Structure
project-folder/
│
├── index.html
├── pages/
│   └── index.css
├── scripts/
│   └── index.js
├── images/
└── README.md

🧠 Key Concepts Demonstrated

Dynamic DOM generation

JavaScript template cloning

Event delegation & event listeners

Modal state management

Class toggling

Clean separation of HTML, CSS, and JS

Reusable component creation via functions

🌍 Live Preview (Optional)

If deployed (GitHub Pages), include:

https://yourusername.github.io/project-name/

🎯 Learning Outcomes

This project demonstrates the ability to:

Build reusable UI components

Manage state through JavaScript

Implement interactive modals

Work with structured data arrays

Follow scalable front-end architecture principles

📎 Author

Eljan Ibrahimli
Software Engineering Student | DevOps Path
