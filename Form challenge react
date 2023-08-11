import "./styles.css";
import { useState } from "react";

const initialState = {
  userName: "",
  fullName: "",
  age: ""
};
export default function App() {
  const [form, setValues] = useState(initialState);

  const [display, setDisplay] = useState(false);

  const printValues = (e) => {
    e.preventDefault();
    setDisplay(true);
  };

  const updateField = (e) => {
    setValues({
      ...form,
      [e.target.name]: e.target.value
    });
  };

  return (
    <form onSubmit={printValues}>
      <div>
        <label htmlFor="userName">
          Username:
          <input
            value={form.userName || ""}
            name="userName"
            onChange={updateField}
          />
        </label>
      </div>
      <br />
      <div>
        <label htmlFor="fullName">
          FullName:
          <input
            value={form.fullName || ""}
            name="fullName"
            type="text"
            onChange={updateField}
          />
        </label>
      </div>
      <br />
      <div>
        <label htmlFor="age">
          Age:
          <input value={form.age || ""} name="age" onChange={updateField} />
        </label>
      </div>
      <br />
      <button>Submit</button>
      {display && (
        <>
          <h4>Request Sent to DB with below request data</h4>
          <ul>
            <li>UserName: {form.userName.toUpperCase()}</li>
            <li>FullName: {form.fullName.toUpperCase()}</li>
            <li>Age: {form.age}</li>
          </ul>
        </>
      )}
    </form>
  );
}
