# Exercise 02: Reviews

Practice working with Objects and Arrays to create a dynamic review system.

## Instructions

Open `main.js` and follow the steps in the comments:

1.  **Setup Data:**
    -   An array of objects (`reviews`) is already provided. Each object has a `name`, `rating`, and `text`.

2.  **Select Elements:**
    -   Select the container where reviews will be displayed (`#reviews-container`).
    -   Select the form (`#review-form`) and its input fields (`#name`, `#rating`, `#review`).

3.  **Render Function:**
    -   Create a function `renderReviews()` that:
        -   Clears the container (`innerHTML = ""`).
        -   Loops through the `reviews` array.
        -   For each review, creates a new `div` with class `review-item`.
        -   Sets the `innerHTML` of this div using the template provided in `index.html`.
        -   Appends the new div to the container.

4.  **Initial Render:**
    -   Call `renderReviews()` once when the page loads to see the initial data.

5.  **Handle Form Submission:**
    -   Add a `"submit"` event listener to the form.
    -   **Prevent Default:** Use `e.preventDefault()` to stop the page from reloading.
    -   **Create Object:** Make a new review object using values from the input fields. *Remember to convert the rating to a number!*
    -   **Update Data:** `push` the new object into the `reviews` array.
    -   **Update View:** Call `renderReviews()` again to display the new list.
