# Class 27

## Django Models

Django web applications access and manage data through Python objects referred to as models. Models define the *structure* of stored data.

Models are usually defined in an application's **models.py** file. They are implemented as subclasses of django.db.models.Model, and can include fields, methods and metadata.

### Fields

```python
my_field_name = models.CharField(max_length=20, help_text='Enter field documentation')
```

The above example has a single field called `my_field_name`, of type `models.CharField`
 — which means that this field will contain strings of alphanumeric character. 

The field types can also take arguments that further specify how the field is stored or can be used. In this case we are giving our field two arguments:

- `max_length=20` — States that the maximum length of a value in this field is 20 characters.
- `help_text='Enter field documentation'` — helpful text that may be displayed in a form to help users understand how the field is used.

The field name is used to refer to it in queries and templates. Fields also have a label, which is specified using the `verbose_name` argument (with a default value of `None`). If `verbose_name`is not set, the label is created from the field name by replacing any underscores with a space.

Common field args and types listed on [MDN](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Models) 

### Metadata

```python
class Meta:
ordering = ['-my_field_name']
```

One of the most useful features of this metadata is to control the *default ordering*
 of records returned when you query the model type. You do this by specifying the match order in a list of field names to the `ordering`
 attribute

Another common attribute is `verbose_name`

### **Methods**

**in every model you should define the standard Python class method `__str__()` to return a human-readable string for each object.** This string is used to represent individual records in the administration site,

Another common method to include in Django models is `get_absolute_url()`, which returns a URL for displaying individual model records on the website

```python
def get_absolute_url(self):
"""Returns the URL to access a particular instance of the model."""
return reverse('model-detail-view', args=[str([self.id](http://self.id/))])
```

Once you've defined your model classes you can use them to create, update, or delete records, and to run queries to get all records or particular subsets of records

To create a record you can define an instance of the model and then call `save()`

```python
#Create a new record using the model's constructor.
record = MyModelName(my_field_name="Instance #1")
#Save the object into the database.
record.save()
```

## Admin

The Django admin *application* can use your models to automatically build a site area that you can use to create, view, update, and delete records. This can save you a lot of time during development, making it very easy to test your models and get a feel for whether you have the *right* data

It is only necessary to *register* you models in order to them to the admin application using “admin.site.register’

In order to log into the admin site, we need a user account with *Staff*
 status enabled. In order to view and create records we also need this user to have permissions to manage all our objects. 

You can create a "superuser" account that has full access to the site and all needed permissions using **manage.py.**

```python
python3 [manage.py](http://manage.py/) createsuperuser
```

To login to the site, open the */admin* URL.

To change how a model is displayed in the admin interface you define a [ModelAdmin](https://docs.djangoproject.com/en/4.0/ref/contrib/admin/#modeladmin-objects)
 class (which describes the layout) and register it with the model.

Once you've got a lot of items in a list, it can be useful to be able to filter which items are displayed. This is done by listing fields in the `list_filter` attribute

All notes taken from MDN.
