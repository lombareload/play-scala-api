Festivities Api
=================================

Required software
--------
- Java 8
- Scala 2.11.7 ~ 2.11.8
- Activator ~1.3.7

Execution
=========

- to run the project from the command line cd into the project directory and run `activator run`

Api
===

- Example calls:

    - Create
    curl -H "Content-Type: application/json" -X POST -d '{"name":"The Name", "place":"The Place", "start":"2016-02-15T05:00:00Z", "end":"2016-02-15T05:00:00Z"}' localhost:9000/festivities

    - Update
    curl -H "Content-Type: application/json" -X PUT -d '{"name":"Fabians event","place":"Harrison fords castle","start":"2016-02-15T05:00:00Z","end":"2016-07-03T05:00:00Z"}' localhost:9000/festivities/1000

    - Query by place and name
    curl localhost:9000/festivities/place/Bowman\'s%20joint
    curl localhost:9000/festivities/name/Bryan\'s%20event

    - Query by dates
    curl localhost:9000/festivities/start/2015-11-15T05:00:00Z
    curl localhost:9000/festivities/end/2015-11-15T05:00:00Z
    curl localhost:9000/festivities/between/2014-11-15T05:00:00Z/2015-11-15T05:00:00Z
