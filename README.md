# Registration Form (React)

A simple, responsive user registration form built using React. This component captures user inputs for first name, last name, email, and password, and provides basic form validation with visual confirmation upon successful submission.

---

## Features

* React functional component using hooks (`useState`)
* Real-time form input handling
* Basic client-side validation
* Success message upon submission
* Clean and minimal styling

---

## Project Structure

```
project-root/
├── src/
│   └── RegistrationForm.js
├── public/
├── README.md
└── ...
```

---

## Installation & Setup

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Start the Application

```bash
npm start
```

### 4. Import the Component

Make sure to use the `RegistrationForm` component inside your main `App.js`:

```jsx
import RegistrationForm from './RegistrationForm';

function App() {
  return (
    <div>
      <RegistrationForm />
    </div>
  );
}

export default App;
```

---

## Code Overview

The component uses the `useState` hook to manage form state:

```js
const [form, setForm] = useState({
  firstName: '',
  lastName: '',
  email: '',
  password: '',
});
```

On input change, the form state is updated:

```js
const handleChange = (e) => {
  const { name, value } = e.target;
  setForm((prevForm) => ({
    ...prevForm,
    [name]: value,
  }));
};
```

On submit, it logs the form and shows a success message:

```js
const handleSubmit = (e) => {
  e.preventDefault();
  console.log('Form submitted:', form);
  setSubmitted(true);
};
```

---

## Technologies Used

* React.js
* JavaScript (ES6+)
* HTML5
* Inline CSS Styling

---








