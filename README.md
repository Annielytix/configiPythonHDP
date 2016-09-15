# Configuring iPython in Hortonworks Sandbox (HDP 2.3.2)
Setting up Hortonworks sandbox for ML including installing and configuring iPython, pySpark and MlLib / ML

There are several prerequisite files that need to be installed. I am using CentOS and yum for this process:

          yum install nano centos-release-scl zlib-devel</li>

          yum install bzip2-devel openssl-devel ncurses-devel

          yum install sqlite-devel readline-devel tk-devel

          yum install gdbm-devel db4-devel libpcap-devel xz-devel

          yum install libpng-devel libjpg-devel atlas-devel

OR

you can install them all at once using the following command:

          yum install nano centos-release-SCL zlib-devel \
          bzip2-devel openssl-devel ncurses-devel \
          sqlite-devel readline-devel tk-devel \
          gdbm-devel db4-devel libpcap-devel xz-devel \
          libpng-devel libjpg-devel atlas-devel

Next, IPython has a requirement for Python 2.7 or higher. Therefore we need to install the “Development tools” dependency for Python 2.7:

          yum groupinstall "Development tools"

Next, install Python2.7

          yum install python27
          
We have to select which version of Python we want to use --> Python 2.7:

          source /opt/rh/python27/enable
          
Next, download and install pip (this will simply adding python packages in future, IMHO):

          wget https://bootstrap.pypa.io/get-pip.py

Install:

          python get-pip.py
          
Use pip to install the most common data science packages (again, IMHO):

          pip install numpy scipy pandas \
          scikit-learn tornado pyzmq \
          pygments matplotlib jsonschema \
          
          pip install jinja2 --upgrade
          
          
          
