# Final-Project-project-03

# Hadoop MapReduce Analysis - Books Set


* The given data set is available at openlibrary.org.
* Now we are going to analyze the book set file using hadoop.
* This is Location we need to dump: http://openlibrary.org/data/ol_dump_works_latest.txt.gz

# Below, i wrote a detailed instructions how to use the code on hadoop server which supports HadoopStreamingAPI

As it has large data(8GB), so we are going to analyse it using hadoop streaming API

* Go to home directory
* First, clone these repository either using https or ssh on to the hadoop server
* After cloning is made, you can view both of our mapper and reducer programs
* Then run the below command on hadoop cluster by making small modifications in  output path where you want to store 

# The following commands are required to run the analysis after cloning the python files into CS Cloud 

* Basic MapReduce Recipe (Python) cmdline:

hadoop jar /usr/local/hadoop/share/hadoop/tools/lib/hadoop-streaming-2.7.1.jar -input /data/openlibrary/ol_dump_works_latest-20161202.txt -output /users-cloud-16fs/kattaha/project3-out/output2 -mapper ~/project3/mapper.py -reducer ~/project3/reducer.py -file ~/project3/{mapper,reducer}.py

After successful execution of hadoop jobs, the output statistics can be viewed in hdfs using below command

* To view the output file

hdfs dfs -cat /users-cloud-16fs/kattaha/project3-out/output2/part-00000
