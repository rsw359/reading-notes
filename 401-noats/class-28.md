# Class 28

## Django forms

A form is a group of one or more fields/widgets on a web page, which can be used to collect information from users for submission to a server.

Forms are a flexible mechanism for collecting user input because there are suitable widgets for entering many different types of data, including text boxes, checkboxes, radio buttons, date pickers.

```html
<form action="/team_name_url/" method="post"><label for="team_name">Enter name: </label><input id="team_name" type="text" name="name_field" value="Default name for team."><input type="submit" value="OK"></form>
```

The `submit` input will be displayed as a button by default. This can be pressed to upload the data in all the other input elements in the form to the server (in this case, just the `team_name` field). The form attributes define the HTTP `method` used to send the data and the destination of the data on the server (`action`):

- `action`: The resource/URL where data is to be sent for processing when the form is submitted. If this is not set (or set to an empty string), then the form will be submitted back to the current page URL.
- `method`: The HTTP method used to send the data: *post* or *get*.
  - The `POST` method should always be used if the data is going to result in a change to the server's database, because it can be made more resistant to cross-site forgery request attacks.
  - The `GET` method should only be used for forms that don't change user data (for example, a search form). It is recommended for when you want to be able to bookmark or share the URL.

The role of the server is first to render the initial form state — either containing blank fields or pre-populated with initial values. After the user presses the submit button, the server will receive the form data with values from the web browser and must validate the information.

The main things that Django's form handling does are:

1. Display the default form the first time it is requested by the user.
    - The form may contain blank fields if you're creating a new record, or it may be pre-populated with initial values (for example, if you are changing a record, or have useful default initial values).
    - The form is referred to as *unbound* at this point, because it isn't associated with any user-entered data (though it may have initial values).
2. Receive data from a submit request and bind it to the form.
    - Binding data to the form means that the user-entered data and any errors are available when we need to redisplay the form.
3. Clean and validate the data.
    - Cleaning the data performs sanitization of the input fields, such as removing invalid characters that might be used to send malicious content to the server, and converts them into consistent Python types.
    - Validation checks that the values are appropriate for the field (for example, that they are in the right date range, aren't too short or too long, etc.)
4. If any data is invalid, re-display the form, this time with any user populated values and error messages for the problem fields.
5. If all data is valid, perform required actions (such as save the data, send an email, return the result of a search, upload a file, and so on).
6. Once all actions are complete, redirect the user to another page.

The `Form` class is the heart of Django's form handling system. It specifies the fields in the form, their layout, display widgets, labels, initial values, valid values, and (once validated) the error messages associated with invalid fields.

To create a `Form`, we import the `forms` library, derive from the `Form` class, and declare the form's fields. Then you can edit the Views, Template, and URL configurations.
