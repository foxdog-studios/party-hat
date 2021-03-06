Party hat
=========

A Web-enabled party hat.

![A partying
duck](https://raw.github.com/foxdog-studios/party-hat/master/webapp/public/shortcut-icon.png)

An example of a [meteor](http://meteor.com) app that connects to an
[Arduino](http://arduino.cc). Originally created for
a workshop at the [Numbers That Matter hackathon](http://numbersmatter.info/).

- [Video demo](https://vine.co/v/MbDVpzlLOvY)


Setup
-----

If you're using a Linux based or OSX system, follow the instructions below. If
you're using a Window system, install [Ubuntu](http://www.ubuntu.com/desktop),
then follow the instructions below. If you're using another system, try the
instructions below and let me know how it goes.

This has been tested with an Arduino Uno with StandardFirmata installed. To
install StandardFirmata using the Arduino IDE, go to `File -> Examples ->
Firmata -> StandardFirmata`.


1.  Ensure you have the following programs installed. You may use your system's
    package manager (preferred) of retrieve them from the Web.

    * A POSIX compliant shell, e.g., bash (you almost certainly have one
      already).

    * [Git](http://git-scm.com/downloads)

    * [Python 2.7](https://www.python.org/download/releases/2.7.6/)

    * [cURL](http://curl.haxx.se/download.html) (you probably already have
      this).

    * [virtualenv](http://www.virtualenv.org/en/latest/) for Python 2.7


2.  Clone the Party hat repository.

    ```shell
    $ git clone https://github.com/foxdog-studios/party-hat.git
    ```

3.  Change your working directory to be the repository.

    ```shell
    $ cd party-hat
    ```

5.  Run the setup script. This will install Meteor, create a Python 2.7 virtual
    environment and install the required Python packages.

    ```shell
    $ ./setup.sh
    ```

Running
-------

1. Launch the controller website by running;

    ```shell
    $ cd webapp
    $ meteor
    ```

    from the root of the repository.

2. Connect an Arduino board to your system and find it's device path. On my
   system, this can be done by running;

   ```shell
   $ ls /dev/ttyACM*
   /dev/ttyACM0
   ```

3. Launch the hat controller by run;

    ```shell
    $ . venv/bin/activate
    $ python hat_controller.py $DEVICE_PATH
    ```

    from the root of the repository. Replace `$DEVICE_PATH` with the path you
    found in step 2.

4. Finally, launch a browser and navigate to `http://localhost:3000`.

