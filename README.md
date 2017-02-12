# pentaho-demo
This project provides a demonstration of capabilities of Pentaho PDI

This  project ingests a .csv file into a MongoDB, computes several summary results, and provides the results in an email.

The .csv file was obtained from https://www.denvergov.org/opendata/dataset/city-and-county-of-denver-traffic-accidents (Traffic Accidents - Comma-Separated Values) on Sunday 12 February 2017.

This project was developed using Pentaho PDI Community Edition 7.0.0.0 and Mongo DB Community Edition 3.4.2

The source files are in the traffic directory.

1.  From Pentaho PDI UI (Spoon) create a File Repository for the project
2.  Copy the following content to the root directory of the File Repository created in step 1:
      * DataIngest.ktr
      * DataExtracts.ktr
      * TrafficAccidents.kjb
      * traffic_accidents.csv
3.  Open the TrafficAccidents job and edit properties (paramaters tab) as follows:
      * Revise project.relative.path to match the location of the File Repository created in step 1.
      * Configure email (smtp) settings as necessary.  The smtp.user and smtp.password parameters must be set.
          For Gmail, access to less secure apps must be allowed.
      * Set email.from and email.to.
4.  Ensure a local instance of mongoDB is running on port 27017.
5.  Run the TrafficAccidents job.
