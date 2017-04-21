# Data Science on Apache Spark

A step-by-step introduction to data science based on Apache Spark and BigDL framework. 

### Topics
* Simple Multiplication
* Linear Regression
* Logistic Regression
* Multilayer Perceptron
* Convolutional Neural Network
* Recurrent Neural Network
* LSTM
* Bi-directional RNN
* Auto-encoder

### Environment

+ Mac OS/Linux
+ Python 2.7
+ Apache Spark 2.1.0
+Jupyter Notebook 

### Download BigDL 0.1.0

+ Spark 2.1.0 and Linux64

https://repo1.maven.org/maven2/com/intel/analytics/bigdl/dist-spark-2.1.0-scala-2.11.8-linux64/0.1.0/dist-spark-2.1.0-scala-2.11.8-linux64-0.1.0-dist.zip
+ Spark 2.1.0 and Mac OS

https://repo1.maven.org/maven2/com/intel/analytics/bigdl/dist-spark-2.1.0-scala-2.11.8-mac/0.1.0/dist-spark-2.1.0-scala-2.11.8-mac-0.1.0-dist.zip

Once you've downloaded above file, unzip it in some directory. 

### Run Jupyter
You can launch the Jupyter notebook as follows:

```
export PYSPARK_DRIVER_PYTHON=jupyter
export PYSPARK_DRIVER_PYTHON_OPTS="notebook --notebook-dir=./ --ip=* --no-browser"
export BigDL_HOME= where the downloaded file unzipped.
```
```
$ source ${BigDL_HOME}/bin/bigdl.sh
$ pyspark \
  --master local[4] \
  --properties-file ${BigDL_HOME}/conf/spark-bigdl.conf \
  --py-files ${BigDL_HOME}/lib/bigdl-0.1.0-python-api.zip \
  --jars ${BigDL_HOME}/lib/bigdl-0.1.0-jar-with-dependencies.jar \
  --conf spark.driver.extraClassPath=${BigDL_HOME}/lib/bigdl-0.1.0-jar-with-dependencies.jar \
  --conf spark.executor.extraClassPath=${BigDL_HOME}/lib/bigdl-0.1.0-jar-with-dependencies.jar
```
If succeed, you can navigate the Jupyter notebook using your browser.
