# *Intro to Django*

- Object-relational mapper

    enables you to interact with your database, like you would with SQL. In fact, Django's ORM is just a pythonical way to create SQL to query and manipulate your database and get results in a pythonic fashion. its let you define your data models entirely in Python, you get dynamic database access API for free.

  - Example:

    ```python
    class Band(models.Model):
        """A model of a rock band."""
        name = models.CharField(max_length=200)
        can_rock = models.BooleanField(default=True)


    class Member(models.Model):
        """A model of a rock band member."""
        name = models.CharField("Member's name", max_length=200)
        instrument = models.CharField(choices=(
                ('g', "Guitar"),
                ('b', "Bass"),
                ('d', "Drums"),
            ),
            max_length=1
        )
        band = models.ForeignKey("Band")
    ```

- URLs and views

    In a high-quality web application, a clean, attractive URL system is a crucial component. Django emphasizes attractive URL design and avoids using crufty extensions like.php or.asp in URLs.
    You construct a URLconf Python module to design URLs for an application. It offers a simple mapping between URL patterns and your views, similar to a table of contents for your app.

  - Example:

    ```python
    from django.urls import path

    from . import views

    urlpatterns = [
        path('bands/', views.band_listing, name='band-list'),
        path('bands/<int:band_id>/', views.band_detail, name='band-detail'),
        path('bands/search/', views.band_search, name='band-search'),
    ]

    from django.shortcuts import render

    def band_listing(request):
        """A view of all bands."""
        bands = models.Band.objects.all()
        return render(request, 'bands/band_listing.html', {'bands': bands})
    ```

- Templates

    The template language in Django is designed to find a balance between power and simplicity. It's intended for folks who are familiar with HTML, such as designers and front-end developers, to feel at ease and learn quickly. However, it is also adaptable and expandable, allowing developers to customize the template language as needed.

    Example:

    ```HTML
    <html>
        <head>
            <title>Band Listing</title>
        </head>
        <body>
            <h1>All Bands</h1>
            <ul>
            {% for band in bands %}
            <li>
                <h2><a href="{{ band.get_absolute_url }}">{{ band.name }}</a></h2>
                {% if band.can_rock %}<p>This band can rock!</p>{% endif %}
            </li>
            {% endfor %}
            </ul>
        </body>
    </html>
    ```

- Forms
    Django comes with a robust form module that can render forms as HTML, validate user-submitted data, and transform it to native Python types. Django also allows you to create and edit data by using forms generated from your existing models.

  - Example:

    ```python
    from django import forms

    class BandContactForm(forms.Form):
        subject = forms.CharField(max_length=100)
        message = forms.CharField()
        sender = forms.EmailField()
        cc_myself = forms.BooleanField(required=False) 
    ```

- Authentication

    Django includes a robust and secure authentication system. User accounts, groups, permissions, and cookie-based user sessions are all handled by it. This allows you to quickly design websites that allow users to create accounts and log in/out safely.

  - Example:

    ```python
    from django.contrib.auth.decorators import login_required
    from django.shortcuts import render

    @login_required
    def my_protected_view(request):
        """A view that can only be accessed by logged-in users"""
        return render(request, 'protected.html', {'current_user': request.user})
        
    ```

- Admin

    Django's automatic admin interface is one of its most powerful features. It reads metadata from your models to provide a robust, production-ready interface that content creators may use to begin managing content on your site right now. It's simple to set up and has a lot of hooks for customization.

  - Example:

    ```python
    from django.contrib import admin
    from bands.models import Band, Member

    class MemberAdmin(admin.ModelAdmin):
        """Customize the look of the auto-generated admin for the Member model"""
        list_display = ('name', 'instrument')
        list_filter = ('band',)

    admin.site.register(Band)  # Use the default options
    admin.site.register(Member, MemberAdmin)  # Use the customized options
    ```

- Internationalization
    Django provides comprehensive text translation support as well as locale-specific formatting of dates, times, numerals, and time zones. It allows app developers and template authors to declare which sections of their apps should be translated or formatted for local languages and cultures, and it uses these hooks to localize web apps for specific users based on their choices.
    -Example:

    ```python
    from django.shortcuts import render
    from django.utils.translation import gettext

    def homepage(request):
        """
        Shows the homepage with a welcome message that is translated in the
        user's language.
        """
        message = gettext('Welcome to our site!')
        return render(request, 'homepage.html', {'message': message})
        
    ```

    ```html
        <!-- {% load i18n %} -->
        <html>
        <head>
            <title>{% trans 'Homepage - Hall of Fame' %}</title>
        </head>
        <body>
            {# Translated in the view: #}
            <h1>{{ message }}</h1>
            <p>
            {% blocktrans count member_count=bands.count %}
            Here is the only band in the hall of fame:
            {% plural %}
            Here are all the {{ member_count }} bands in the hall of fame:
            {% endblocktrans %}
            </p>
            <ul>
            {% for band in bands %}
            <li>
                <h2><a href="{{ band.get_absolute_url }}">{{ band.name }}</a></h2>
                {% if band.can_rock %}<p>{% trans 'This band can rock!' %}</p>{% endif %}
            </li>
            {% endfor %}
            </ul>
        </body>
        </html>
    ```

- Security

Django protects you from a variety of threats, including:

- Clickjacking
- Site-to-site scripting
- Forgery of Cross-Site Requests (CSRF)
- Injection of SQL
- Remote code execution

-------------

## *How Django Works Behind the Scenes*

Django is a Python-based web framework that is utilized by millions of developers and billions of users via popular apps such as Instagram. It is open source, which means that the code may be downloaded for free from Github and used alongside the official documentation by any developer. However, I've found that even experienced Django developers have little understanding of "how" Django is truly run, both technically and legally/financially.
