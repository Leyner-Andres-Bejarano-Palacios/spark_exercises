# spark_exercises

## this image looks simple enough

https://hub.docker.com/r/apache/spark-py

getting the working directory
- import os
- os.getcwd()

things that I would like to know of the sparkContext ??????
- sc

copying files to container
- docker cp README.md 7c5fa20a3cc9:/opt/spark/work-dir/README.md
- docker exec -it --user root 7c5fa20a3cc9 bash
- sc.textFile("README.md").count()
- lines = sc.textFile("README.md")
- lines.first()
- dockerHubLines = lines.filter(lambda line: "hub.docker.com" in line)
- dockerHubLines.first()
- lines = sc.parallelize(["hello world","hi","world"])
- words = lines.flatMap(lambda line: line.split(" "))
- words.first()
- words.count()
- uniqueWords = words.distinct()
- uniqueWords.count()
- countingRdd = sc.parallelize([1,2,3,4])
- countingRdd.countByValue().collect()
- SomeTuples = sc.parallelize([(1,2),(3,4),(3,6)])
- SomeTuples.reduceByKey(lambda x,y: x+y ).collect()
- SomeTuples.groupByKey().collect()
- SomeTuples.map(lambda x: (x[0],x[1]+1)).collect()
- SomeTuples.map(lambda x: (x[0],x[1]+1)).collect()