## User Study Verification Institutes
Verification Institutes is a browser app to simulate cast-as-intended verification with the Benaloh Challenge.
The verification institutes belong to the [prototype](https://github.com/Yonjuni/benaloh-challenge-usability-study) which was used in a usability study of the Benaloh Challenge.

### Institute Old
This page corresponds to the original Helios Single Ballot Verifier. But be aware, that it is a dummy based on the single page apps in the Repo benaloh-challenge-usability-study. Thus, verification is only mocked.

### Institute One
This page corresponds to an improvement suggestion for ballot verification. Instead of copying and pasting verification-related data, this data is transfered to the verification institute automatically.   


## Download and more Information

### Building 

Requirements:
* Python 3.5
* Django 1.11

There are two options of hosting the application: With or without virtualenv 

If you intend to use virtualvenv, navigate to your desired directory and start by: 

    pyvenv venv
    source venv/bin/activate

On a production server this probably is located somewhere in /var/www , on a developers computer this normally is located somewhere in your $HOME.

Now you can clone the sourcecode of the application into your directory:

    https://github.com/SECUSO/user-study-verification-institutes.git

After that you should have a subdirectory institutes/ and if you created a virtualenv also a subdirectory env/. The actual application are is in the verification/ directory. Please navigate into the institutes directory. 

The application itself is done, but you need to initialize your database. You can canfigure institutes/settings.py to use mySQL or PostGreSQL described here. Or you can leave the file as it is to use sqlite. 

Initialize your database with

    ./manage.py makemigrations
    ./manage.py migrate
    ./manage.py migrate --run-syncdb
    
    
Start a development Server
--------------------------
If you intend to make some changes, you can start the application now with

    python manage.py runserver
    
The application can be accessed under the url `http://localhost:8000`.


## License

User Study Verification Institutes is licensed under the GPLv3. Copyright (C) 2017-2018 Karola Marky

This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, either version 3 of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with this program. If not, see http://www.gnu.org/licenses/.
