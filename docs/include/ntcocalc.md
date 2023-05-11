# Remote: Jupyter Hub and CoCalc

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

## NT Jupyterhub serverer

Website: https://ntprog2.upb.de

We have our own Jupyter Hub server (https://ntprog2.upb.de), but we have to activate your University Account (i.e. IMT account) manually.
If its not activated, you will get the following error:

> Spawn failed: Server at http://127.0.0.1:46431/jupyter/user/<IMTUser\>/ didn't respond in 30 seconds
 
Ask your tutor, to get your account activated. He needs your IMT login name.
Alternatively, your can ask your tutor to get a user and password assigned.

## IMT Jupyterhub server

Website: https://jupyter.upb.de

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

Inside the university are more Jupyterhub servers, but we have no permissions to
use them for teaching. You have to ask the maintainer, whether it is ok to use them.

# Remote: CoCalc

While this software provides nice colaborative features, the docker image they provide is unstable.
We stopped to recommend our CoCalc server, because randomly the projects of the students freeze.
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
   - Note: Our CoCalc server doesn't send a confirmation email, your account will directly be appoved after registration.
   - Use the lecture name as prefix of your first name (e.g. `[SML] Max`). That ensures your tutor will be able to invite you to the correct projects.
   -  If you visit multiple lecture, you can use something like `[SML][DSSP] Max`.

## FAQ

Q: When I open a Notebook, it asks `Select a Kernel`
A: Simply select the suggested kernel `Python 3 (Ubuntu Linux)`

Q: What is a kernel?
A: The kernel could be interpreted as the executer of the notebook. Everything that should be executed is send to the kernel. There are options for different Python installations, but also for other laguages `R` or `Octave`.
   
