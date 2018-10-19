title:      Creating a New Project
desc:       The official docnado installation guide. 
date:       2018/10/11
version:    1.0.0
template:   document
nav:        Before You Begin>Creating a New Project
percent:    100
authors:    enq@heinventions.com


Now that you have install docnado you're ready to start your new project. Do do this you should navigate to a new directory where you want your documentation to live and run our handy built in generation script.
```bash
$ mkdir ~/documentation_project
$ cd documentation_project
$ docnado --new
```
This will create a basic example of a documentation project using docnado, and demonstrate all of it's useful features. Just run:
```bash
$ docnado 
 * Serving Flask app "docnado.docnado" (lazy loading)
 * Environment: production
   WARNING: Do not use the development server in a production environment.
   Use a production WSGI server instead.
 * Debug mode: off
 * Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)
```

And visit [http://127.0.0.1:5000](http://127.0.0.1:5000) to see docnado in action.
