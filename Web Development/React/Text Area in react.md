Here is an example of making a text area component being made in [[Forms in react]]

```
import React, { useState } from 'react';

const MyForm = () => {
  // State to manage the value of the textarea
  const [textareaValue, setTextareaValue] = useState('');

  // Event handler to update the state when the textarea value changes
  const handleTextareaChange = (event) => {
    setTextareaValue(event.target.value);
  };

  // Event handler to handle form submission
  const handleSubmit = (event) => {
    // Prevent the default form submission behavior
    event.preventDefault();

    // Do something with the textarea value, for example, log it
    console.log('Textarea value submitted:', textareaValue);
  };

  return (
    <form onSubmit={handleSubmit}>
      <label>
        Your Message:
        {/* Controlled TextArea component */}
        <textarea
          value={textareaValue}
          onChange={handleTextareaChange}
          rows="4"
          cols="50"
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