# MIS_Project

AA 2022/2023

## Members

Roberto Mazzaro
Laura Corso
Noemi Canovi
Mattia Carolo

## Topic

The scope of this project is to analyze reflex phenomena through the implementation of a multisensory interactive system. To achieve this the project must be paired with his physical counterpart.

In order for the project to work

### Can You run it

In order 

### How To Start

P.S. Remember that each time a component prompts for a password it is 
MIS@DISI

>> Windows

1) access through terminal to the PI (it should be connected to the local network) with SSH
2) Once inside launch the server with the command 'vncserver'. It should build the address at the same IP with the port 1
3) Access through 'vnc viewer' to the PI using the address found before 

>> PI Launch

- go to path $:> MIS_project>Server
- launch python3 app.py --host=0.0.0.0
- launch celery -A app.celery worker --loglevel=info --pool threads
- launch pd (not with &)
- check audio in test audio e media
- launch Main_osc