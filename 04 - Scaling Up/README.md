For the purpose of solving Homework 3, you will have to configure your jupyter notebook and anaconda installations to run pyspark. To do so, you need to perform the following:

1) Install java (at least version 8) if they are not installed already

2) Select a folder to install spark:
```bash
export SPARK_HOME=<selected_dir>
```
(for example, to install Spark under /opt/spark, do export SPARK_HOME=/opt/spark)

**You will have to execute this command in the beggining of each shell session or add it to your configuration.**

3) [Download](https://spark.apache.org/downloads.html) one of the [prebuilt Spark packages for Hadoop](https://www.apache.org/dyn/closer.lua/spark/spark-2.3.2/spark-2.3.2-bin-hadoop2.7.tgz). Navigate to the folder you saved the .tgz file and extract it sing the following commands:

```bash
mkdir -p $SPARK_HOME
tar -xzf spark-*-bin-hadoop*.tgz --directory $SPARK_HOME --strip-components 1
```

4) Make sure your JAVA_HOME is configured correctly:
```bash
$JAVA_HOME/bin/java -version
```
should complete without an error.

If you get an error you can set JAVA_HOME for the current shell session using:
```bash
export JAVA_HOME=<path_to_my_java_home_folder>
```
where `<path_to_my_java_home_folder>` is the parent folder of `bin/java`, as for example `/usr/lib/jvm/java-8-oracle`

5) Activate your ada environment:
```bash
source activate ada
```

6) Configure your conda installation using:
```bash
conda install -c conda-forge pyspark findspark
```

7) Start a jupyter session:
```bash
jupyter notebook
```

8) Inside your notebook locate and import (py)spark by adding in a cell:
```python
import findspark
findspark.init()
import pyspark
```

9) Enjoy Spark!
