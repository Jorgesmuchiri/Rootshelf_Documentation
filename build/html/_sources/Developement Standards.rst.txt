Developement Standards 
======================

General programming
*******************
Rootshelf has been nuilt using Websauna, It is  a full stack Python web framework for building consumer and community oriented websites.
Websauna gives you building blocks for creating scalable, state-of-the-art websites and services. The framework enables efficient business problem solving, so that developers can maximize productivity from day zero. Websauna is suggestive and has default options on all parts of stack, so one can follow a red line to get the first release out quickly. On the other hand, Websauna does not enforce hard opinions and sacrifice flexibility, so that experienced developers can easily override parts and use more sophisticated components for specific needs.

Websauna achieves flexibility by keeping its own codebase minimal and not reinventing the wheel. Instead it provides a polished integration of the top packages of Python ecosystem like Pyramid web framework, SQLAlchemy object relationship mapper, Alembic migration scripts, IPython shell, Authomatic federated login, Jinja templating and pytest testing framework.

Websauna is focused on Internet facing sites where you have a public or private sign up process and administrative backend. It’s sweet spots are custom business portals, software-as-a-service sites and consumer portals. A special focus is given for security, so that Websauna is a strong candidate for financial technology and eCommerce solutions

* **References**
	* `Documentation <https://docs.websauna.org/index.html#/>`_


Database
********

Rootshelf uses PostgreSQL which is a powerful, open source object-relational database system that uses and extends the SQL language combined with many features that safely store and scale the most complicated data workloads.

PostgreSQL comes with many features aimed to help developers build applications, administrators to protect data integrity and build fault-tolerant environments, and help you manage your data no matter how big or small the dataset. In addition to being free and open source, PostgreSQL is highly extensible. For example, you can define your own data types, build out custom functions, even write code from different programming languages without recompiling your database!

* **References**
	* `Documentation <https://www.postgresql.org/docs/>`_


Github
******

#. Create a branch from the master for the same change. The branch name should be descriptive
#. Once fixed, create a pull request asking a specific person to review the feature
#. Reviewed and approved features should be merged back to the master and the branch deleted
#. You can link to a line of code, or a section of code by reading `here <https://gist.github.com/briankip/c2fb1d40873fc644ed66>`_
#. There are config files that you want to change but don't want to commit, i.e ``/app/config/app.php`` and ``/app/config/database.php`` you can prevent yourself from accidentally commiting these files by doing ``git update-index --assume-unchanged /path/to/file.ext`` your changes will no longer be tracked. [`Read more here <http://archive.robwilkerson.org/2010/03/02/git-tip-ignore-changes-to-tracked-files/>`_]



Database
========


