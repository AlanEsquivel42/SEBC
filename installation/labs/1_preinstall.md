**HOLA MARKDOWN**

hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar terasort -Dmapred.map.tasks=4 -Dmapred.reduce.tasks=4 -Dmapred.reduce.tasks.speculative.execution=false terasort-input terasort-output
hadoop jar /opt/cloudera/parcels/CDH/lib/hadoop-0.20-mapreduce/hadoop-examples.jar teragen -Dmapred.map.tasks=4 -Dmapred.map.tasks.speculative.execution=false 100000000 terasort-input

Inline-style: 
![alt text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 1")