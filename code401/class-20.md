# Django Models

## *Using models*

Models are Python objects that Django web applications use to access and manage data. Models determine the structure of stored data, including field types and optionally their maximum size, default values, selection list options, documentation help text, form label text, and so on. The model is defined independently of the underlying database, which you can select from a list of options in your project settings. You don't need to talk to the database directly once you've decided which one to use — all you have to do now is write your model structure and other code, and Django will handle the dirty work of talking with the database for you.

- Model definition
Models are often defined in the models.py file of an application. They are implemented as django.db.models.Model subclasses and can contain fields, methods, and metadata. A "typical" model, named MyModelName:, is shown in the code excerpt below.

```python
from django.db import models

class MyModelName(models.Model):
    """A typical class defining a model, derived from the Model class."""

    # Fields
    my_field_name = models.CharField(max_length=20, help_text='Enter field documentation')
    ...

    # Metadata
    class Meta:
        ordering = ['-my_field_name']

    # Methods
    def get_absolute_url(self):
        """Returns the url to access a particular instance of MyModelName."""
        return reverse('model-detail-view', args=[str(self.id)])

    def __str__(self):
        """String for representing the MyModelName object (in Admin site etc.)."""
        return self.my_field_name
```

- Fields
Each field in a model represents a column of data that we wish to store in one of our database tables. A model can contain an arbitrary number of fields of any type. One of each field value will be present in each database record (row). Take a look at the following example:

```python
my_field_name = models.CharField(max_length=20, help_text='Enter field documentation')
```

> my_field_name is ty of models.CharField, which means that this field will contain strings of alphanumeric characters.

> max_length=20 — States that the maximum length of a value in this field is 20 characters.
> help_text='Enter field documentation' — provides a text label to display to help users know what value to provide when this value is to be entered by a user via an HTML form.

## Metadata

You can declare model-level metadata for your Model by declaring class Meta, as shown.

```python
class Meta:
    ordering = ['-my_field_name']
```

Controlling the default ordering of records returned when querying the model type is one of the most helpful capabilities of this metadata. As seen above, you achieve this by setting the match order in a list of field names in the ordering attribute. The order of the fields will be determined by the type of field (character fields are sorted alphabetically, while date fields are sorted in chronological order). To reverse the sorting order, precede the field name with a negative symbol (-), as seen above.