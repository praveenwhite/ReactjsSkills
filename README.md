# ReactjsSkills

To make the test more **typical** while incorporating **Redux** for state management, the task can be designed to evaluate the candidate's ability to use Redux effectively in a React.js app. Redux is commonly used in real-world applications to manage global state across multiple components, making this a practical test for developers with 5 years of experience.

### 1-Hour Machine Test (React.js + Redux):

**Objective**: Assess the candidate's ability to integrate Redux for state management in a React.js app that performs basic CRUD operations with API integration.

### Question:
**Task**: Build a small **product management dashboard** using React and Redux. The application should allow users to **view**, **add**, **update**, and **delete** products. The app should use Redux to manage the global state and communicate with a simple REST API.

---

#### **Part 1: Set Up Project and Redux (15 minutes)**

1. **Setup a New React Project**:
   - Use **Create React App** or **Vite** to set up the project.
   - Install the following libraries:
     - `redux`
     - `@reduxjs/toolkit`
     - `react-redux`
     - `axios` (for API requests)

2. **Create a Basic Redux Store**:
   - Use **Redux Toolkit** to set up a Redux store.
   - Create a `products` slice with the following initial state:
     - `products` (an array of product objects)
     - `loading` (boolean to handle loading states)
     - `error` (string for error messages)
   - Create asynchronous thunks for the following actions:
     - `fetchProducts` (GET /products)
     - `addProduct` (POST /products)
     - `updateProduct` (PUT /products/:id)
     - `deleteProduct` (DELETE /products/:id)

---

#### **Part 2: CRUD Functionality (30 minutes)**

1. **Product List**:
   - Fetch and display the list of products from the API.
   - Dispatch `fetchProducts` action when the component loads.
   - Use `useSelector` to access the `products` state from Redux.
   - Display the following product details in a table or list:
     - `name`
     - `price`
     - `category`
   - Provide **edit** and **delete** buttons for each product.
   - Implement loading and error states, using `loading` and `error` from the Redux state.

2. **Add Product Form**:
   - Create a form that allows users to add a new product with the following fields:
     - `name`
     - `price`
     - `category`
   - Dispatch `addProduct` action to add a new product to the backend and Redux store.
   - After adding a product, the product list should automatically update.

3. **Edit Product**:
   - Allow users to edit an existing product by dispatching the `updateProduct` action.
   - Prefill the form with the selected product's details for editing.
   - After updating, the product list should reflect the changes.

4. **Delete Product**:
   - Allow users to delete a product by dispatching the `deleteProduct` action.
   - Confirm before deleting, and update the product list afterward.

---

#### **Part 3: Bonus Task (Optional - 15 minutes)**

1. **Pagination (Optional)**:
   - Implement pagination to handle large lists of products.
   - Fetch products in pages by dispatching `fetchProducts` with `page` and `limit` parameters.

2. **Testing**:
   - Write basic unit tests for the Redux slice using **Jest** or **React Testing Library**.
   - Test at least one action creator and the product reducer.



### **Evaluation Criteria**:
- **Redux Integration**: Proper use of Redux Toolkit for managing global state and asynchronous actions.
- **API Integration**: Correct handling of API requests using `axios` and Redux thunks.
- **State Management**: Efficient use of `useSelector` and `useDispatch` for accessing and updating the Redux store.
- **Component Structure**: Clean and well-organized component structure with proper use of hooks.
- **CRUD Operations**: Fully functional Create, Read, Update, and Delete actions, with seamless state updates in the UI.
- **Loading and Error Handling**: Graceful handling of loading states and errors during API requests.
- **Code Quality**: Clean, readable, and maintainable code.
- **Bonus**: Pagination, testing, or performance optimizations (if implemented).

This test gives a realistic sense of the candidate's ability to work with React and Redux in typical use cases, such as managing global state, performing asynchronous operations, and handling CRUD actions.
