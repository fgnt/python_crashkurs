# Remote: Jupyter Hub, CoCalc, Colab and JupyterLite

## Options

While Python can be installed on a local machine or on a network filesystem,
there are plenty of options to program in a Browser.

Options:
 - Jupyter Hub installations in the university
   - ZIM: https://jupyter.upb.de
   - Noctua: https://jh.pc2.uni-paderborn.de (Requires HPC access)
 - CoCalc: https://cocalc.com (US company)
 - Colab: https://colab.google (US company)
 - JupyterLite: https://jupyter.org/try-jupyter/lab/
   - May not support all scientific packages
   - Runs locally and uses the browser cache to store files.

While we recommend using a local installation, a remote installation
is often comfortable to use across multiple computers.
The listed Jupyter Hubs are operated by someone in the university (ZIM, HPC),
and hence we recommend using those. But note, that they don't have data backups.
If you want to have data backups, we recommend using the Poolroom computers,
that have backups for the home directory.


# Remote: Jupyter Hub

[jupyter.org](https://jupyter.org/hub):

> JupyterHub brings the power of notebooks to groups of users.
> It gives users access to computational environments and resources 
> without burdening the users with installation and maintenance tasks.
> Users - including students, researchers, and data scientists - can
> get their work done in their own workspaces on shared resources which
> can be managed efficiently by system administrators.
>
> JupyterHub runs in the cloud or on your own hardware, and makes it
> possible to serve a pre-configured data science environment to any
> user in the world. It is customizable and scalable, and is suitable
> for small and large teams, academic courses, and large-scale infrastructure.

<!--- We stopped our Jupyterhub server, because the IMT has one
## NT Jupyterhub server

Website: https://ntprog2.upb.de

We have our own Jupyter Hub server (https://ntprog2.upb.de), but we have to activate your University Account (i.e. IMT account) manually.
If its not activated, you will get the following error:

> Spawn failed: Server at http://127.0.0.1:46431/jupyter/user/<IMTUser\>/ didn't respond in 30 seconds
 
Ask your tutor, to get your account activated. He needs your IMT login name.
Alternatively, your can ask your tutor to get a user and password assigned.
-->

## ZIM (formerly IMT) Jupyterhub server

Website: https://jupyter.upb.de

 - IMT login
 - Select Scientific python environment, Datascience environment or Tensorflow environment


### Setup:

See https://hilfe.uni-paderborn.de/Jupyter_-_Allgemeine_Informationen for instructions with pictures.
When someone finds the instructions in english, please inform us.

Here a summary (When I switched the language to english, the website had still the German field names):

 - Go to https://serviceportal.uni-paderborn.de.
   - Click on "Benutzerverwaltung" and "Weitere Dienste".
   - Activate "Erweiterte Ansicht".
   - Search for "Jupyter" and click "Optionen" and then "Beantragen".
 - Go to https://jupyter.upb.de
   - Login with IMT credentials
   - Select Scientific python environment.

## Other Jupyterhub servers

Inside the university are more Jupyterhub servers, but we have no permission to
use them for teaching. You have to ask the maintainer, whether it is ok to use them.

<!---

# Remote: CoCalc

While this software provides nice collaborative features, the docker image they provide is unstable.
We stopped recommending our CoCalc server because randomly the projects of the students freeze.
For https://cocalc.com/ we observed no stability problems.

(Wikipedia)[https://en.wikipedia.org/wiki/CoCalc]: 
> CoCalc (formerly called SageMathCloud) is a web-based cloud computing (SaaS) and course management platform for computational mathematics.
> Part of the Sage project, it supports editing of Sage worksheets, LaTeX documents and Jupyter notebooks. 
> CoCalc runs an Ubuntu Linux environment that can be interacted with through a terminal, additionally giving access to most of the capabilities of Linux.
> 
> CoCalc offers both free and paid accounts.
> Subscriptions starting at $14/month provide internet access and more storage and computing resources.
> One subscription can be used to increase quotas for one project used by multiple accounts.
> There are subscription plans for courses. Over 200 courses have used CoCalc.


For remote programming exercises we decided to use CoCalc. 
We have our own server. Therefore, the service is completely free of charges. but to use this server you are still
required to create an account. 
Look up the URL and registration token in the online couse management (Panda) or ask your tutor if you occur any problems.

Step by step registration:
 - Open the URL.
 - Click *Sign In*
 - Fill `Create an Account`
   - Note: Our CoCalc server doesn't send a confirmation email, your account will directly be approved after registration.
   - Use the lecture name as prefix of your first name (e.g. `[SML] Max`). That ensures your tutor will be able to invite you to the correct projects.
   -  If you visit multiple lectures, you can use something like `[SML][DSSP] Max`.

-->


# Use CoCalc
[https://cocalc.com/](https://cocalc.com/) Collaborative Calculation in the Cloud

 - Open a browser
 - Go to [https://cocalc.com/](https://cocalc.com/)
 - Log in
 - Open a project
 - Go to settings
 - Launch the Plain Jupyter server.

You can also use the build in Jupyter, but it misses some features.


# FAQ

Q: When I open a Notebook, it asks `Select a Kernel` <br/>
A: Simply select the suggested kernel, e.g. `Python 3 (Ubuntu Linux)`

Q: What is a kernel? <br/>
A: The kernel could be interpreted as the executor of the notebook.
Everything that should be executed is sent to the kernel.
There are options for different Python installations, but also for other languages `R` or `Octave`.

Q: What happened with the department jupyterhub server? <br/>
A: Since ZIM has now a Jupyter Hub server with a proper integration of the university account, we recomment to use that one.
