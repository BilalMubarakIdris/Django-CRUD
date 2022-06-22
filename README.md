# Django-CRUD

[Django CRUD]

 

Create a new GitHub repository with a README.md, and Python .gitignore file.

Clone it to your machine/computer, that will create a new folder on your computer with your repository’s content.

Create a new virtual environment in that folder named env and install django in it.

Create a new django project. Use your Zuriboard Student ID as the name of the project.

Create a new application using the django startapp command. The app should be called blog.

Add the blog app to the main_projects INSTALLED_APPS.

 

Replace the content of blog/models.py with the content of this starter file: https://github.com/TobeTek/Zuri/blob/main/starter-files/Django-CRUD/models.py . We should now have a Post model in blog/models.py.

Create migrations for your new model using the makemigrations django command. 

Run all migrations using, migrate django command.

To make our Post model accessible from the admin site, register the Post model in blog/admin.py 

 

Now for the views. 

In blog/views.py,  create a new view/class PostListView, which inherits django’s generic ListView,  it’s config/attributes should be:

model = Post

 

Create another view, PostCreateView, which inherits django’s generic CreateView, with attributes:

model = Post

fields = “__all__”

success_url  = reverse_lazy(“blog:all”)

 

Create another view, PostDetailView, which inherits django’s generic DetailView, with attributes:

model = Post

 

Create another view PostUpdateView, which inherits django’s generic UpdateView, with attributes:

model = Post

fields = “__all__”

success_url  = reverse_lazy(“blog:all”)

 

Create another view PostDeleteView, which inherits django’s generic UpdateView, with attributes:

model = Post

fields = “__all__”

success_url  = reverse_lazy(“blog:all”)

 

Time to create templates.

Create a new folder templates under the blog app.  

Copy all the files and folders from https://github.com/TobeTek/Zuri/tree/main/starter-files/Django-CRUD/templates to blog/templates folder.

 

Create a file, blog/urls.py, if it doesn’t already exist.

Replace the content of blog/urls.py with the content of https://github.com/TobeTek/Zuri/blob/main/starter-files/Django-CRUD/urls.py 

 

Go to your project_app/urls.py and add a new url pattern with the following content:

path("blog/", include("blog.urls", namespace="blog"))

 

Stage and Commit your Django project and push your changes to your GitHub repository. 

Do not add your database (db.sqlite) to version control (GitHub). 

Ensure your final code/submission is on the default branch of your GitHub repository.

Submit the link to your Github repository e.g https://github.com/github_username/repo_name

 

Resources:


Django CRUD Functionality with CBVS CLASS BASED VIEWS 

Working with the Terminal 

Python Functions 

Django CRUD (Create, Retrieve, Update, Delete) Function Based Views - GeeksforGeeks 
