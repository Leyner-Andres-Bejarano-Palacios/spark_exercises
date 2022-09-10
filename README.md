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
