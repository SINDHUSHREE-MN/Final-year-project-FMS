Create-Flask-App PRs Welcome Flask port of create-react-app that is used for initializing project structure of your next application.

Creating an app - How to create a new app. Create Flask app works on macOS, Windows and Linux. If something doesn't work, please file an issue. If you have questions, suggestions or need help, feel free to open an issue.

Quick overview pip install createflaskapp create-flask-app my-app cd my-app # activate venv python run.py (use correct version of pip and python according to your OS and python install) Then open http://localhost:5000 to see your app. When you are ready to deploy to production, set environment variable PRODUCTION to True on your server of choice, clone the project onto your server and spin it up.

Creating an app You'll need to have Python 3.6 or higher on your local development machine (but it's not required on the server). To create a new app, you can run :

bash create-flask-app my-app python python -m create-flask-app my-app It will create a directory called my-app inside the current folder. Inside that directory, it will generate the initial project structure :

my-app/ ├──venv ├── app │ ├── __init__.py │ ├── config.py │ ├── errors │ │ ├── __init__.py │ │ └── handlers.py │ ├── home │ │ ├── __init__.py │ │ └── routes.py │ ├── static │ │ └── css │ │ └── main.css │ └── templates │ ├── about.html │ ├── base.html │ ├── error.html │ └── home.html ├── requirements.txt └── run.py No complicated configuration or folder structures, only the files you need to build and deploy your app. Once the installation is done, you can open your project folder:

cd my-app Inside the newly created project, you can run some commands:

source venv/bin/activate or .venvScriptsactivate Activates the virutal environment required for the project dependency isolation.

Read more about venv.

pip install -r requirements.txt Installs libraries and dependencies listed in requirements.txt in active environment.

python run.py Starts the app in development mode. Open http://localhost:5000 to view it in browser.

The page will automatically reload if you make changes to the code. You will see errors in app reload or startup in the console.

##############################################Installation via virtual environment#####################################################################################

Installation Python Version We recommend using the latest version of Python. Flask supports Python 3.7 and newer.

Dependencies These distributions will be installed automatically when installing Flask.

Werkzeug implements WSGI, the standard Python interface between applications and servers. Jinja is a template language that renders the pages your application serves. MarkupSafe comes with Jinja. It escapes untrusted input when rendering templates to avoid injection attacks. ItsDangerous securely signs data to ensure its integrity. This is used to protect Flask's session cookie. Click is a framework for writing command line applications. It provides the flask command and allows adding custom management commands. Optional dependencies These distributions will not be installed automatically. Flask will detect and use them if you install them.

Blinker provides support for :doc:`signals`. python-dotenv enables support for :ref:`dotenv` when running flask commands. Watchdog provides a faster, more efficient reloader for the development server. greenlet You may choose to use gevent or eventlet with your application. In this case, greenlet>=1.0 is required. When using PyPy, PyPy>=7.3.7 is required.

These are not minimum supported versions, they only indicate the first versions that added necessary features. You should use the latest versions of each.

Virtual environments Use a virtual environment to manage the dependencies for your project, both in development and in production.

What problem does a virtual environment solve? The more Python projects you have, the more likely it is that you need to work with different versions of Python libraries, or even Python itself. Newer versions of libraries for one project can break compatibility in another project.

Virtual environments are independent groups of Python libraries, one for each project. Packages installed for one project will not affect other projects or the operating system's packages.

Python comes bundled with the :mod:`venv` module to create virtual environments.

Create an environment Create a project folder and a :file:`venv` folder within:

.. tabs::

   .. group-tab:: macOS/Linux

      .. code-block:: text

         $ mkdir myproject
         $ cd myproject
         $ python3 -m venv venv

   .. group-tab:: Windows

      .. code-block:: text

         > mkdir myproject
         > cd myproject
         > py -3 -m venv venv


Activate the environment Before you work on your project, activate the corresponding environment:

.. tabs::

   .. group-tab:: macOS/Linux

      .. code-block:: text

         $ . venv/bin/activate

   .. group-tab:: Windows

      .. code-block:: text

         > venv\Scripts\activate

Your shell prompt will change to show the name of the activated environment.

Install Flask Within the activated environment, use the following command to install Flask:

$ pip install Flask Flask is now installed. Check out the :doc:`/quickstart` or go to the :doc:`Documentation Overview </index>`.
