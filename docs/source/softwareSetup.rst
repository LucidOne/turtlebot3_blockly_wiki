.. _chapter_softwareSetup:

Software Setup
==============

This software setup is for the advanced users who would like to create their custom blocks to either add new funtionalities or modify the existing ones.

The following steps were adapted from the instructions provided by `Erle Robotics <http://erlerobotics.com/blog/>`_.


Installation
************

Linux
~~~~~

Open terminal and enter the following instructions to install and develop blockly.
::

    $ mkdir -p ~/blockly_ws/src
    $ cd ~/blockly_ws/src
    $ git clone https://github.com/dabit-industries/turtlebot3_blockly
    $ cd robot_blockly/frontend/
    $ git clone https://github.com/erlerobot/ace-builds.git
    $ git clone https://github.com/dabit-industries/blockly.git
    $ cd ~/blockly_ws/
    $ catkin_make_isolated -j2 --pkg turtlebot3_blockly --install

or
~~
::

    $ mkdir -p ~/blockly_ws/src
    $ cd ~/blockly_ws/src
    $ git clone --recurse-submodules https://github.com/dabit-industries/turtlebot3_blockly
    $ cd ..
    $ catkin_make_isolated -j2 --pkg turtlebot3_blockly --install

Launch
******
::

    $ source ~/blockly_ws/devel_isolated/setup.bash
    $ roslaunch turtlebot3_blockly turtlebot3_blockly.launch

.. NOTE::
  To launch the web interface of blockly, you don't necessarily have to start ``roscore`` but you should if you plan to connect Turtlebot3 and test it during development.