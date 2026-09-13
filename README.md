# DevStack

DevStack is a React-based web application where users can explore different developer tools and add their favorite tools to their personal stack. The project is designed with a clean and responsive user interface.

## Technologies Used

* React
* TypeScript
* Vite
* Tailwind CSS
* React Icons
 
## Features

 ## demo link :GitHub Repository Link: https://github.com/Nazu3872/Assignment-5-B14.git
## Live Site Link: https://nazu3872.github.io/Assignment-5-B14/
  

* **Explore Developer Tools** — Users can browse different developer tools with useful information such as name, category, rating, and description.
* **Add Tools to Stack** — Users can add their favorite tools to their personal stack.
* **Manage Selected Tools** — Users can view the tools they have selected and remove them from the stack when needed.

---

# React Questions & Answers

## 1. What is JSX, and why is it used in React?

JSX is a syntax that allows us to write HTML-like code inside JavaScript or TypeScript. It makes React components easier to write and understand.

## 2. What is the difference between props and state?

**Props** are used to pass data from a parent component to a child component. Props are read-only.

**State** is data managed inside a component. When state changes, React updates the UI.

## 3. What does the `useState` hook do, and where did you use it in this project?

`useState` is a React Hook used to create and manage component state.

I used `useState` to manage the selected products in the stack. When a product is added or removed, the state changes and the UI updates.

## 4. What does the `useEffect` hook do, and why did you need it to load the JSON data?

`useEffect` is used to perform side effects in a React component.

I used `useEffect` to load the product data from the JSON file when the application starts.

## 5. Why does every item in a `.map()` list need a unique `key` prop?

A unique `key` helps React identify each item in a list. It helps React efficiently update the correct items when the list changes.

## 6. What is conditional rendering? Show one place you used it.

Conditional rendering means displaying different UI based on a condition.

For example, I used it to show an empty stack message when no product has been selected.

```tsx
{selectedProducts.length === 0 ? (
  <p>Your stack is empty.</p>
) : (
  selectedProducts.map((product) => (
    <Product key={product.id} product={product} />
  ))
)}
```

## 7. How do you pass data from a parent component to a child component, and how does a child send something back to the parent?

A parent component passes data to a child component through **props**.

To send something back to the parent, the parent can pass a function as a prop. The child can then call that function with the required data.

For example:

```tsx
<Product
  product={product}
  handleAddToStack={handleAddToStack}
/>
```

Here, `product` and `handleAddToStack` are passed from the parent component to the child component.
