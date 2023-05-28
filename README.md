# MIS_Project

AA 2022/2023

## Members

Noemi Canovi; Mattia Carolo; Laura Corso; Roberto Mazzaro.

## Topic

As part of Multisensory Interactive Systems course, run by prof. Turchet in University of Trento, an
interactive system involving three of the main senses (vision, touch and hearing), has been developed
and tested.
It represents an opportunity for sportsmen and others to sharpen their reaction time and improve their
hand-eye coordination. Indeed, it is an automatic training tool in which tennis balls fall from a platform
and the user has to catch them before they touch the ground. To aid the reaction response, numerous
cues are presented before the fall, such as vibrations, sounds and lights.
In addition, the timing between the start of the fall and the catch of the user is stored and sent to a
website in order to provide a tool for the monitoring of the training.

To complete the project, this code must be paired with its physical counterpart.

## Structure

The codebase is divided in folders where:

- Server folder will contain both the FrontEnd and BackEnd of our project;
- PureData will have inside the various patches that will be used during the execution;
- TeensyCode will have the source code already uploaded to the Teensy;
- Stats will contain all the scripts to analyze the results obtained during all the experiments.

### Can You run it

In order to run the project you need:

- A Raspberry Pi 4 (check at the beginning if numpy is supported);
- A Teensy board (we used the 3.6 version however all 3.X version should be supported);
- Custom Hardware (check the related [paper](MultisensoryReport.pdf)).

### How To Start

P.S. Remember that each time a component prompts for a password it is 
MIS@DISI

>> Windows & Linux

1) access through terminal to the PI (it should be connected to the local network) with SSH;
2) Once inside launch the server with the command 'vncserver'. It should build the address at the same IP with the port 1;
3) Access through 'vnc viewer' to the PI using the address found before.

>> PI Launch

- go to path $:> MIS_project>Server
- launch python3 app.py --host=0.0.0.0
- launch celery -A app.celery worker --loglevel=info --pool threads
- launch pd (not with &)
- check audio in test audio e media
- launch Main_osc
