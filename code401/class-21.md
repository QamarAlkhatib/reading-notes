# Django Forms

An HTML Form is a collection of one or more fields/widgets on a web page that can be used to collect data from users and send it to a server. Because there are acceptable widgets for entering many different types of data, including as text boxes, checkboxes, radio buttons, date pickers, and so on, forms are a flexible technique for gathering user input. Forms are also a safe way to share data with the server because they allow us to transmit data through POST requests that are protected against cross-site request forgery.

## Django form handling process

Django's form handling employs the same approaches as in earlier tutorials (for displaying information about our models): the view receives a request, does any necessary actions (including reading data from the models), and then builds and delivers an HTML page (from a template, into which we pass a context containing the data to be displayed). What complicates things further is that the server must be able to process data provided by the user and redisplay the page if any problems occur.
Here is a diagram:

![diagram](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Forms/form_handling_-_standard.png)

- Based on the diagram above, the main things that Django's form handling does are:

1. The default form will be displayed the first time the user requests it.

    - If you're establishing a new record, the form may include blank fields, or it may be pre-populated with default values (e.g. if you are changing a record, or have useful default initial values).
    Because it isn't coupled with any user-entered data at this point, the form is referred to as unbound (though it may have initial values).

2. Receive data from a submit request and bind it to the form.

    - When we bind data to a form, we ensure that the user-entered data, as well as any mistakes, are available when the form is re-displayed.

3. Clean and validate the data.

    - Cleaning the data sanitizes the input (for example, deleting invalid characters that may be used to send harmful stuff to the server) and turns it to Python types that are consistent.

    - Validation ensures that the values are appropriate for the field (e.g., that they are within the correct date range, that they aren't too short or lengthy, and so on).

---

## Form

Django's form handling mechanism is built around the Form class. It defines the form's fields, as well as its layout, display widgets, labels, initial values, valid values, and (once validated) error messages for erroneous fields. The class also has methods for displaying itself in templates using predefined forms (tables, lists, and so on) and for obtaining the value of any element (enabling fine-grained manual rendering).

## Declaring a Form

The syntax for declaring a Form is quite identical to that for declaring a Model, and the field types are the same (and some similar parameters). This makes sense since we need to make sure that each field handles the proper types of data, is limited to valid data, and has a description for display and documentation in both cases.

The data from a form is saved in the forms.py file in the application directory. Make a copy of the file locallibrary/catalog/forms.py and open it. We import the forms library, inherit from the Form class, and declare the form's fields to construct a Form. The following is a very basic form class for our library book renewal form; copy and paste it into your new file:

```python
from django import forms

class RenewBookForm(forms.Form):
    renewal_date = forms.DateField(help_text="Enter a date between now and 4 weeks (default 3).")
```
