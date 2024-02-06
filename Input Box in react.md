Here is an example of creating an input box in a [[Forms in react]] 

```
import React, { useState } from 'react';

const MyForm = () => {
  // State to manage the value of the input box
  const [inputValue, setInputValue] = useState('');

  // Event handler to update the state when the input value changes
  const handleInputChange = (event) => {
    setInputValue(event.target.value);
  };

  // Event handler to handle form submission
  const handleSubmit = (event) => {
    // Prevent the default form submission behavior
    event.preventDefault();

    // Do something with the input value, for example, log it
    console.log('Input value submitted:', inputValue);
  };

  return (
    <form onSubmit={handleSubmit}>
      <label>
        Your Name:
        {/* Controlled Input component */}
        <input
          type="text"
          value={inputValue}
          onChange={handleInputChange}
        />
      </label>
      <br />
      {/* Submit button */}
      <button type="submit">Submit</button>
    </form>
  );
};

export default MyForm;

```
#Web-Dev #React #Frontend #javascript 