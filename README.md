wikinomaly
=================

Description
-----------

The goal of this project was to turn [this Netflix java lib](https://medium.com/netflix-techblog/rad-outlier-detection-on-big-data-d6b0494371cc)
into a spark job. 

Code Repository
---------------

https://github.com/mylons/wikinomaly

User Documentation
------------------
Usage: 
```
Anomaly [column name] [number of rows] [number of columns] [force diff] [input csv path]
```
* based on netflix's [example usage](https://github.com/Netflix/Surus/blob/master/resources/examples/pig/rad.pig#L55)
* for more insight on how options are set [see constructor](https://github.com/Netflix/Surus/blob/3f68bd384e2267ca00602febe4a382a55a40eb4d/src/main/java/org/surus/pig/RAD.java#L39-L52)
* and the rest of the code is a literal translation of [this](https://github.com/Netflix/Surus/blob/3f68bd384e2267ca00602febe4a382a55a40eb4d/src/main/java/org/surus/pig/RAD.java#L118-L272)

Requirements
------------

The surus-0.1.4.jar, but it is provided in the `lib` dir of this repo

Tested Configurations
---------------------

Tested on OS X, with spark 2.3.0, Java 1.8

Setup
-----

Integrates cleanly with https://gerrit.wikimedia.org/r/#/admin/projects/analytics

Running Tests
-------------

Uses http://www.scalatest.org/user_guide/using_the_runner

Was run `org.wikimedia.analytics.refinery.job.AnomalySuite` as the main class

Deployment
----------

See Setup

Issue Tracker
-------------

No

To Do
-----

* likely needs to be an s3 path input to the job
* review query at line 53 in Anomaly.scala

Built With
----------

The provided surus jar

Contributors
------------

github.com/blackhoundnate

Contributing
------------

Check it out

Contact
-------

nate@blackhound.io


License
-------

GNU General Public License

Copyright
---------

Copyright © 2018 President and Fellows of Harvard College
