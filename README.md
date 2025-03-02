form {
  display: flex;
  flex-direction: column;
  gap: 16px;
  max-width: 500px;
  margin: auto;
  padding: 20px;
  background: #f5f5f5; /* Light grey background */
  border-radius: 10px;
  box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
}

mat-form-field {
  width: 100%;
}

input, textarea {
  background: white !important; /* White background for inputs */
  border-radius: 5px;
}

textarea {
  min-height: 100px;
  resize: vertical;
}

button {
  width: 100%;
  padding: 10px;
  font-size: 16px;
}
