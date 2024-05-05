- To create an admin:
  - python manage.py createsuperuser
 
- Admin dashboard:
  - http://127.0.0.1:8000/admin


- To make an app modifiable in the admin dashboard:
  - In appName/admin.py:
    - admin.site.register(ModelName)
  - Now the app should be displayed in the admin dashboard, allowing us to
    create, update and remove objects.

- Current user:
  - joaquin.tornello
  - 12345678