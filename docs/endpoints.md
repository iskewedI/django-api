- To create a full usable endpoint that hosts some webpage:
  - In the appDir/views.py create the view.
  - In the appDir/urls.py declare an array called urlpatterns.
    - urlpatterns = [
      path("", views.index, name="index"),
    ]
    - This will map every URL pattern with the view to render.
  - In the site/urls.py include the app URL in the site.
    - path("appName/", include("appName.urls")),