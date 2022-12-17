# In hdfs file system / is the root

# Command to check the files inside root hdfs directory
hadoop fs -ls /

# Command to create directory in hdfs
hadoop fs -mkdir /input_data


# Copy data from local file system to Hdfs
hadoop fs -put test_demo/trees.csv /input_data

# Copy from HDFS path to local file system
hadoop fs -copyToLocal /input_data/trees.csv ./

# Command to execute map reduce code
hadoop jar hadoop-streaming-2.4.0.jar -files mapper.py,reducer.py -mapper mapper.py -reducer reducer.py -input /test/demo.txt -output /output
