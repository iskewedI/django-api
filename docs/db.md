- The database is configured under site/settings.py
  - They are specified in the DATABASES variable

- To create the database tables:
  - python manage.py migrate
  - This will 'migrate' the apps specified in the INSTALLED_APPS settings.py variable.
  - This creates the db.sqlite3 file.

- Models:
  - Single, definitive source of information about your data.
  - Here we define the data scheme.
  - They are defined in the appName/models.py file

  - With them, Django is able to:
    - Create a database schema (CREATE TABLE statements) for this app.
    - Create a Python database-access API for accessing Question and Choice objects.

- We need to add our app into the project INSTALLED_APPS settings.py variable:
  - INSTALLED_APPS = [
      "appName.apps.AppNameConfig",
      ...
  ]

  - And then, to create models in our new app:
    - python manage.py makemigrations appName
    - 'makemigrations' tells django we've made changes in our models, and we'd like
      the changes to be stored as a migration.
    - This creates the files inside the appName/migrations directory.

    - Then, run python manage.py migrate again, to apply the new migrations in our  project.

  - To see the SQL of an app 
    - python manage.py sqlmigrate appName 0001


- To query data:
  - from polls.models import ModelName
  - ModelName.objects.all() # To get all the objects
  - m = ModelName(...args) # To instantiate a new object
  - m.save() # To save the new object
  - m.custom_method(...args) # Execute a custom method