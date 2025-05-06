## Overview

**Recipe Finder** is a web application designed to help users find and explore recipes based on ingredients, dietary preferences, and more. The app allows users to search for recipes, view detailed information such as the title, publisher, preparation time, servings, and ingredients, and save their favorite recipes. Users can also adjust the number of servings for a recipe, and the app will automatically update the ingredient quantities to match. The app is fully responsive, ensuring a smooth experience on both desktop and mobile devices. It's built using JavaScript, HTML, and Sass to provide an interactive and user-friendly interface.

## How the Code Works

The project is structured into multiple files, each playing a specific role in the functionality and layout of the application. Here's an overview of how the code is organized and how the different parts work together:

* **JS Directory**: Contains the main logic of the application.

  * `model.js` handles the core data logic (fetching, storing, and managing recipes).
  * `controller.js` manages the interaction between the model and the views, ensuring that the right data gets passed to the UI.
  * `helpers.js` includes utility functions that simplify common tasks, such as formatting or error handling.
  * `config.js` stores configuration settings like API endpoints or constants that are used throughout the app.
  * `views/` contains separate JavaScript files that manage the rendering of different UI components (e.g., search bar, recipe view, pagination).

* **Sass Directory**: Holds the styling for the application, written in Sass for easier CSS management.

  * `_base.scss` defines the foundational styles for the application (e.g., resets, typography).
  * `_components.scss` handles the styling for reusable UI components like buttons, cards, and modals.
  * `_header.scss`, `_preview.scss`, `_recipe.scss`, and other partials define the look and feel of specific parts of the app (e.g., search results, recipe pages, and uploads).
  * `main.scss` imports all the partials to compile the final CSS.

* **Images**: The `img/` folder contains the assets used in the UI, like the app's favicon and logo.

## Features

* **Recipe Search**: Allows users to search for recipes by ingredient, cuisine, or name.

* **Recipe Details**: Users can view detailed information about each recipe, including ingredients, instructions, and nutritional facts.

  * **Recipe Data**: The detailed recipe includes:

    * **Title**: The name of the recipe.
    * **URL**: A link to the recipe’s page.
    * **Image URL**: The image URL of the recipe.
    * **Publisher**: The publisher or source of the recipe.
    * **Prep Time**: Time required to prepare the recipe.
    * **Servings**: Number of servings the recipe makes.
    * **Ingredients**: A list of ingredients, with each entry in the format:

      ```
      Quantity, Unit, Description
      ```

      Example:

      * Ingredient 1: `0.5, kg, Rice`
      * Ingredient 2: `1, , Avocado`
      * Ingredient 3: `, , Salt`
      * Ingredient 4: `Quantity, Unit, Description`

* **Adjustable Servings**: Users can modify the number of servings they want for a recipe. The app will automatically adjust the ingredient quantities accordingly. For example, if the original recipe serves 4 and you want to scale it to 8 servings, the app will double the ingredient quantities, making it easier to scale recipes for larger gatherings or smaller portions.

* **Bookmarks**: Users can save their favorite recipes and revisit them later.

* **Pagination**: The app supports pagination for search results, making it easier to browse through multiple pages of recipes.


## Usage

To run the app locally, follow these steps:

1. Clone the repository:

   ```
   git clone https://github.com/AmaanP314/recipe-finder.git
   ```

2. Navigate to the project directory:

   ```
   cd recipe-finder
   ```

3. Install dependencies:

   ```
   npm install
   ```

4. Start the development server:

   ```
   npm start
   ```

5. Open your browser and go to `http://localhost:3000` to view the app.

## Tech Stack

* **HTML5**: For structuring the content and layout of the pages.
* **CSS3 / Sass**: For styling the app with a modular approach.
* **JavaScript**: For handling the dynamic functionality, including fetching recipe data, managing user interactions, and updating the UI.
* **Node.js**: For running the development environment and managing dependencies through npm.
* **API**: The app fetches data from [recipe API](https://forkify-api.herokuapp.com/).

## Live App:

**[Recipe Finder](https://forkify-ten-sooty.vercel.app/)**
