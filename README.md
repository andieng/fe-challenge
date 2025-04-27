## Challenge: Searchable List Component

### Objective

Build a reusable React.js component that displays a list of items with a search feature, using the JSONPlaceholder API to fetch data.

### Requirements

- **Functionality**:
  - Create an input field for users to enter a search keyword.
  - Display a list of **Users** (fetched from https://jsonplaceholder.typicode.com/users) filtered by the search keyword in real-time (no submit button needed).
  - If the search keyword is empty, show the full list of Users.
  - Filter should match the `name` field of the User model (e.g., "Leanne Graham").
  - Enable inline editing of the user's username field:
    - Click the username to edit.
    - On blur or Enter, save changes locally (no real backend call needed).
    - Reflect changes instantly (optimistic UI).
  - Implement undo for the last username change (one level of undo).
- **Technical**:
  - Use React hooks (`useState`, and others as needed) for state management.
  - Ensure the component is **reusable** (can accept a list of items via props).
  - Handle loading and error states (e.g., show "Loading..." or "Error fetching data").
- **UI**:
  - Minimal styling required (ensure the input and list are clear).
  - (Optional) Use basic CSS or Tailwind CSS or anything that you want for styling if desired.
- **API**:

  - Use https://jsonplaceholder.typicode.com/users to fetch User data.
  - Example User model:

    ```json
    { "id": 1, "name": "Leanne Graham", "username": "Bret", "email": "Sincere@april.biz", ... }
    ```

- **Time**: 30 minutes (live coding).
- **Output**: Working code demonstrating the search functionality. It doesn't need to be perfect, but should show your approach and thought process.
