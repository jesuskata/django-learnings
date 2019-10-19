# This is a README file to include inside all the commands and important learnings from Django framework

- [This is a README file to include inside all the commands and important learnings from Django framework](#this-is-a-readme-file-to-include-inside-all-the-commands-and-important-learnings-from-django-framework)
  - [Important commands](#important-commands)
    - [How to create a Virtual Environment](#how-to-create-a-virtual-environment)
    - [Watching our installed libraries](#watching-our-installed-libraries)
    - [Installing Django and creating a new project](#installing-django-and-creating-a-new-project)
    - [Debugging tool](#debugging-tool)
    - [Creating an application](#creating-an-application)
    - [Template System](#template-system)
    - [Design pattern](#design-pattern)

## Important commands

### How to create a Virtual Environment

- With the included method from Python3

```bash
python -m venv <name-of-virtual-environment>
# For example
python -m venv .venv
```

### Watching our installed libraries

```bash
pip freeze
pip list
```

### Installing Django and creating a new project

```bash
# For installing the last version
pip install django -U
```

Once installed, we have a new command `django-admin`. So, now we can create a new folder for our project:

```bash
mkdir <project>
cd <project>
```

And now we can create our django project

```bash
django-admin startproject <projectname> . # With this, the project will be created inside our actual folder
```

### Debugging tool

Inside your url you can import a debugger with:

```django
import pdb; pdb.set_trace()
```

### Creating an application

Inside your actual project folder you can do:

```bash
# Is important to do the name of the apps in plural name
./manage.py startapp posts
```

### Template System

You can see more in [here](https://docs.djangoproject.com/en/2.2/ref/templates/builtins/)

Is a form to present the data using html. It includes a little bit of logic. Now, is important to remember:

_urls_: are in charge to find the resources, looking to match with the petition and doing the relation with the view that will do the response to that.

_views_: is in charge of the logic to find the data.

_template_: is in charge of the logic to present the data. They are defined in the `settings.py` in the `TEMPATES` section.

### Design pattern

Is a reusable solution to a common problem.

One of the Web common design patterns is the **MVC (Model View Controller)**. Separating the data, from the presentation, from the logic.

_controller_: manage the logic of the request. It knows what to do, and what template needs to be shown. The controller is in charge to change the data through the model.

_model_: is in charge to define the data structure, the access to them and the validation.

_view_: is in charge to see how to present the data, to show them to the user.

**Django** use a design pattern called the MTV (Model Template View).

_model_: do the same as the MVC above 👆.

_template_: is the logic of the presentation.

_view_: is in charge of bring data and pass them to the template.
