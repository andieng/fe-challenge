## Challenge: Searchable List Component

### Objective

Build a reusable React.js component that displays a list of items with a search feature, using the JSONPlaceholder API to fetch data.

### Requirements

- **Functionality**:

  1.  Enhanced Search Input:

      - Create an input field for users to enter a search keyword.
      - Display a list of `Users` (fetched from `https://jsonplaceholder.typicode.com/users`).
      - **Debounced Real-time Filtering:** Implement a debounce mechanism (e.g., 300ms-500ms) for the search input. The list should filter _after_ the user pauses typing.
      - **Multi-Field & Case-Insensitive Search:** The filter should match the search keyword against both the `name` and `username` fields of the User model, and it must be case-insensitive.
      - If the search keyword is empty, show the full list of Users.

  2.  Advanced Inline User Editing:
      - Enable inline editing of the user's `username` field.
      - Clicking the username should switch it to an editable input field.
      - On blur or Enter key press, attempt to "save" changes.
      - **Optimistic UI with Rollback:** Reflect changes instantly on the UI (optimistic update). However, _simulate_ a backend save operation that takes 500ms and has a **20% chance of failure**. If the simulated "save" fails, the UI must gracefully revert the username to its previous state.
      - **Multi-Level Undo/Redo:** Implement a robust undo/redo feature for `username` changes. Users should be able to undo multiple previous changes and redo them if desired. This state should be managed locally.

- **Technical**:
  - Utilize React hooks (`useState`, `useEffect`, `useRef`, `useCallback`, and custom hooks as appropriate) for all state management and side effects.
  - Handle API loading and error states gracefully (e.g., show "Loading..." or "Error fetching data").
  - Demonstrate good code organization and separation of concerns (e.g., consider custom hooks for specific logic).
- **UI**:
  - Minimal styling required (ensure the input and list are clear and functional).
  - (Optional) Use basic CSS, Tailwind CSS, or any styling library if desired, but functionality and clean code are prioritized.
- **API**:

  - Use https://jsonplaceholder.typicode.com/users to fetch User data.
  - Example User model:

    ```json
    {
      "id": 1,
      "name": "Leanne Graham",
      "username": "Bret",
      "email": "Sincere@april.biz",
      "...": "..."
    }
    ```

- **Time**: 30 minutes (live coding).
- **Output**: Working code demonstrating the search functionality. It doesn't need to be perfect, but should show your approach and thought process.
