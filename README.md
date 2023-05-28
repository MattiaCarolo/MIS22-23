# MIS_Project

AA 2022/2023

## Members

Roberto Mazzaro
Laura Corso
Noemi Canovi
Mattia Carolo

## Topic

The scope of this project is to analyze reflex phenomena through the implementation of a multisensory interactive system. To achieve this the project must be paired with his physical counterpart.

## Structure

The codebase is divided in folders where:

- Server folder will contain both the FrontEnd and BackEnd of our project.
- PureData will have inside the various patches that will be used during the execution
- TeensyCode will have the source code already uploaded to the teensyy
- Stats will contain all the scripts to analyze the results obtained during all the experiments 

### Can You run it

In order to run the project you need:

- A Raspberry Pi 4 (check at the beginning if numpy is supported)
- A Teensy board (we used the 3.6 version however all 3.X version should be supported)
- Custom Hardware (check the related [paper](MultisensoryReport.pdf))

### How To Start

P.S. Remember that each time a component prompts for a password it is 
MIS@DISI

>> Windows & Linux

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
