# python-wamp
Installation notes for python and wamp server installation

# video
https://www.youtube.com/watch?v=N3XfGXi4ifE

#PYTHON INSTALLATION
Download python 3.6.6 Win64 version
installed @ c:/python366

#WAMP SERVER INSTALLATION
Download wamp server 3.1.3 Win64 version 
installed @ c:/wamp64

modified httpd.conf
..edited "Reqire all none" to "Require all granted" as follow
..<Directory />
    AllowOverride none
    Require all granted
..</Directory>

..add "+ExecCGI" at the end of "Options +Indexes +FollowSymLinks +Multiviews" become
      Options +Indexes +FollowSymLinks +Multiviews +ExecCGI
..uncomment "#AddHandler cgi-script .cgi" and add ".py" becomes
      AddHandler cgi-script .cgi .py
      
#Install python modules
in command windows
  C:/python36
type following commands
..upgrade pip
  python -m pip install --upgrade pip
..install numpy
  python -m pip install numpy for array calculations
..install pandas
  python -m pip install pandas
  
  #python database moudules
..install psycopg2 for connecting with postgresql
  python -m pip install psycopg2
..install mysql connector for connecting with mysql in wamp server
  python -m pip install mysql-connector
  
# kml moudule
..install fastkml and requirements for kml module ..see https://github.com/cleder/fastkml
  python -m pip install fastkml
  python -m pip install lxml
  python -m pip install shapely
