.. _settingup:

Ferret/PyFerret installation on Ubuntu
======================================

a. Create folder on D:\ or E:\ partition
----------------------------------------

For example the folder name is **ferret_training**

b. Download and install miniconda
---------------------------------

- Download Miniconda2-latest-Linux-x86_64.sh file from drive that shared for training participants and locate to folder created above (ex: ferret_training).

- Launch ubuntu and change work directory to Miniconda2-latest-Linux-x86_64.sh file is located.

.. hint:: Hint:
   To check current work directory type ‘pwd’ (without quote) on ubuntu terminal and press enter.

.. figure:: /images/01ferret.png
   :alt: alt text goes here
   :align: center
   
   *check current working directory*

Change work directory to folder that Miniconda2-latest-Linux-x86_64.sh file is located (for ex: E:\Bayu\Training_ferret).

Type ‘**cd file_directory_path**’ (without quote) to change work directory.

.. note::
   
   To change to Windows folder/directory, usually we use ‘../../mnt/’ then followed by partition name and folder name. Example is shown as below:

.. figure:: /images/02ferret.png
   :alt: alt text goes here
   :align: center
   
   *change directory*

Check whether it is in the correct directory. By type ‘**ls -l**’ we should see Miniconda2-latestLinux-x86_64.sh file in this directory.

.. figure:: /images/03ferret.png
   :alt: alt text goes here
   :align: center
   
   *list Miniconda installer code*

Run Miniconda2-latest-Linux-x86_64.sh script use command as followings:

.. code-block:: bash

   ./Miniconda2-latest-Linux-x86_64.sh

The result after press enter will be shown below:
 
.. figure:: /images/04ferret.png
   :alt: alt text goes here
   :align: center
   
   *Run Miniconda shell script*

Press enter several time to review license agreement:

.. figure:: /images/05ferret.png
   :alt: alt text goes here
   :align: center
   
   *Review License Agreement*

Type ‘**yes**’ (without quote) then press enter:

.. figure:: /images/06ferret.png
   :alt: alt text goes here
   :align: center
   
   *Accepting the license terms*

Press enter, after extracting the result will be shown as below:

.. figure:: /images/07ferret.png
   :alt: alt text goes here
   :align: center
   
   *All requested packaged already installed*

Type ‘**yes**’ (without quote) then press enter:

.. figure:: /images/08ferret.png
   :alt: alt text goes here
   :align: center
   
   *Finished of Miniconda installation*

Close ubuntu terminal by type ‘**exit**’ then press enter or click X sign on upper right corner.

c. Download and install Ferret/PyFerret
---------------------------------------

Launch Ubuntu terminal


.. figure:: /images/09ferret.png
   :alt: alt text goes here
   :align: center
   
   *Launch Ubuntu terminal*

Download and install PyFerret using miniconda by type below command and press enter

.. code-block:: bash

   conda create -n FERRET -c conda-forge pyferret --yes

.. figure:: /images/10ferret.png
   :alt: alt text goes here
   :align: center
   
   *Launch Miniconda environment*

PyFerret already installed. To launch ferret, environment where we installed pyferret is needed.

Type below command and press enter to activate this environment

.. code-block:: bash

   source activate FERRET

.. figure:: /images/11ferret.png
   :alt: alt text goes here
   :align: center
   
   *activate FERRET env*

Type ‘ferret’ (without quote) then press enter to launch Ferret in Ubuntu

.. figure:: /images/12ferret.png
   :alt: alt text goes here
   :align: center
   
   *FERRET Launch*

PyFerret already installed but to launch graphical visualization an X server will need to be installed on the Windows 10 system and the DISPLAY variable will need to be set in Bash.

d. Install graphical program on WSL
-----------------------------------

- Make sure to close Ubuntu terminal before you install graphical program on WSL.

- Download XMing software installer from https://xming.en.softonic.com/download or from training shared drive.

- Install XMing by double-click installer file.

.. figure:: /images/13ferret.png
   :alt: alt text goes here
   :align: center
   
   *XMing Setup Wizard*

.. figure:: /images/14ferret.png
   :alt: alt text goes here
   :align: center
   
   *Select components of XMing to be install*

.. figure:: /images/15ferret.png
   :alt: alt text goes here
   :align: center
   
   *Completing the XMing Setup Wizard*

.. tip:: Tip:
   If XMing is properly installed and launched, it will be shown small icon of XMing on Windows taskbar.

.. figure:: /images/16ferret.png
   :alt: alt text goes here
   :align: center
   
   *x*

Once you have an X server installed and running, you'll need to install graphics applications.

.. attention:: Attention:
   To download and install it run the following command on Ubuntu terminal:

.. code-block:: bash

   sudo apt-get install x11-apps


.. figure:: /images/17ferret.png
   :alt: alt text goes here
   :align: center
   
   *XMing active indicator*

Type ‘Y’ and press enter:

.. figure:: /images/18ferret.png
   :alt: alt text goes here
   :align: center
   
   *x11-apps installation*

Once the applications have been installed, you can start them by setting your display and executing the application on the Bash shell.

Type following command on Ubuntu terminal and press enter:

.. code-block:: bash

   export DISPLAY=:0


.. figure:: /images/19ferret.png
   :alt: alt text goes here
   :align: center
   
   *x11-apps installation completed*

e. Automatic ferret environment and WSL graphical activated
-----------------------------------------------------------

- Using ferret environment and WSL graphical may need to comment the lines that launch the conda environment and Windows X server.

- To make it easier, you can add command lines in .bashrc file that located in the home folder.

In a new terminal, type the following:

.. code-block:: bash

   cd ~/
   nano .bashrc

Scroll to the bottom of the file and add following lines

.. code-block:: bash

   conda activate FERRET
   export DISPLAY=:0

.. figure:: /images/20ferret.png
   :alt: alt text goes here
   :align: center
   
   *automatic environment setup*

.. attention:: 

   Press Ctrl+x, press ‘Y’ then press enter.
   Close the terminal by type ‘exit’ and press enter or click X sign on upper right corner.


f. Test installed Ferret/PyFerret
---------------------------------

Open Ubuntu terminal from Windows start menu.

.. figure:: /images/21ferret.png
   :alt: alt text goes here
   :align: center
   
   *Ubuntu Launch*

Type ‘ferret’ (without quote) in ubuntu terminal then press enter.

.. figure:: /images/22ferret.png
   :alt: alt text goes here
   :align: center
   
   *Ferret Launch*

Ferret software is ready to use.

.. tip::

   For checking WSL graphical program that we need to visualize data plot, ferret demonstration script can be used.

The jnl files are "go scripts", available to you when you run Ferret, for example: "GO tutorial" shows you around Ferret.

Type ‘go tutorial’ (without quote) and press enter:

.. figure:: /images/23ferret.png
   :alt: alt text goes here
   :align: center
   
   *go tutorial demo*

Press enter:

.. figure:: /images/24ferret.png
   :alt: alt text goes here
   :align: center
   
   *plot demo*

Press enter several times will show you example of scripts and plot results:

.. figure:: /images/25ferret.png
   :alt: alt text goes here
   :align: center
   
   *plot multiple views demo*

.. figure:: /images/26ferret.png
   :alt: alt text goes here
   :align: center
   
   *vector demo*

.. figure:: /images/27ferret.png
   :alt: alt text goes here
   :align: center
   
   *fill demo*

Type ‘quit’ (without quote) to exit ferret and back to ubuntu terminal.

This is end of installationGuide's document.

GOOD LUCK!!!

