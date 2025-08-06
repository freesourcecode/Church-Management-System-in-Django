# Church Management System Project in Django with Source Code

The **Church Management System Project in Django created based on Python, Django, and SQLITE3 Database**.

The **Church Management System** project created to assist clerics in managing church members and finances from the central office to the branch levels.

It has several modules, the most important of which are the members and admin sections. 

Members maintain their system accounts, Tithes, and other giving’s while the admin has access to all functionality and functionalities of the app.

>[!NOTE]
> To start creating a **Church Management System Project in Python Django**, makes sure that you have PyCharm Professional IDE Installed in your computer.

## Church Management System in Django: Admin Features

* **Register Page**

The page where new user created their login credentials for the website.

* **Login Page**

The page where the system administrator enters their system credentials in order to gain access to the system’s administrative side.

* **New Ministries Page**

This is the page where an administrator can add a new ministries.

* **Ministries List** 

The page with a list of ministries that can be navigated to change or delete a ministries.

* **New Shepherd**

The page to which an administrator can add new shepherd.

* Shepherd List

The page on which the list of shepherd can be viewed, modified, or deleted.

* **New Member**

The page to which an administrator can add new member.

* **Member List**

The page on which the list of member can be viewed, modified, or deleted.

* **New User Page**

The page where a new admin credentials are created by an admin.

* **Users list**

This is the page that lists and manages the added users.

## How to Create a Project Church Management System in Django?

1. **Open file**.

Open “pycharm professional” after that click “file” and click “new project”.

<img width="484" height="453" alt="image" src="https://github.com/user-attachments/assets/d201b2c1-95e2-4926-9112-c45e609c3213" />

2. **Choose Django**.

Next, after click “new project“, choose “Django” and click.

<img width="152" height="325" alt="image" src="https://github.com/user-attachments/assets/415a23f2-534a-4649-8016-7105ca07c316" />

3. **Select file location**.

Then, select a file location wherever you want.

4. **Create application name**.

After that, name your application.

5. **Click create**.

Lastly, finish creating project by clicking “create” button.

6. **Start Coding**.

Finally, we will now start adding functionality to our Django Framework by adding some functional codes.

## Functionality and Codes of the Church Management System Project in Django with Source Code

* **Create template for the add ministries form in Church Management System in Django**.

In this section, we will learn on how create a templates for the add ministries form. 

To start with, add the following code in your add.html under the folder of /templates/ministries.

```
{% extends 'base.html' %}

{% block internal_style %}

    <style>
        .card{
            border-top: 3px solid #f3b600;
        }
    </style>

{% endblock internal_style %}


{% block content %}
    <div class="dashboard-wrapper">
        <div class="container-fluid dashboard-content">
            <div class="col-xl-7 col-lg-10 col-md-11 col-sm-12 col-xl-12 mx-auto">
        {% if messages %}
            {% for message in messages %}
                <div class="col-lg-12 mr-auto ml-auto alert bg-warning alert-dismissable pb-0 pt-0" role="alert">
                    <button type="button" class="close" data-dismiss="alert" aria-label="Close">
                        <span aria-hidden="true" class="text-danger"><b>&times;</b></span>
                    </button>
                    <div class="row">
                        <div class="mr-auto ml-auto">
                        <p class="h5 mr-auto ml-auto p-2 text-light">
                             <b>
                                {% if message.tags ==  "alert-danger" %}
                                    <i class="fa fa-exclamation-triangle mr-3 text-danger"></i> {{ message }}
                                {% else %}
                                    <i class="fa fa-check"></i> {{ message }}
                                {% endif %}
                            </b>
                        </p>
                    </div>
                    </div>
                </div>
            {% endfor %}
        {% endif %}
        <div class="card">
            <h5 class="card-header h5">Add A New Ministry </h5>
            <div class="card-body">
                <form action="{% url 'create_ministry' %}" method="post" class="mb-5">
                    {% csrf_token %}
                    <div class="form-group mb-5">
                        <label for="{{ form.name.id_for_label }}">Ministry Name</label>
                        <input type="text" class="form-control" id="{{ form.name.id_for_label }}" name="{{ form.name.name }}" autofocus required>
                    </div>
                    <div class="form-group mb-5">
                        <label for="{{ form.leader.id_for_label }}">Leader</label>
                        <input type="text" class="form-control" id="{{ form.leader.id_for_label }}" name="{{ form.leader.name }}">
                    </div>
                    <div class="form-group">
                        <label for="{{ form.description.id_for_label }}">Ministry Description</label>
                        <textarea name="{{ form.description.name }}" id="{{ form.description.id_for_label }}" cols="30" rows="10" class="form-control"></textarea>
                    </div>

                    <button class="btn btn-success mt-5 text-light shadow btn-sm">Add Ministry</button>
                </form>
            </div>
        </div>
    </div>
        </div>
    </div>

{% endblock content %}
```

### 📌 Here's the full documentation for the [Church Management System Project in Django](https://itsourcecode.com/free-projects/python-projects/church-management-system-project-in-django-with-source-code/)

