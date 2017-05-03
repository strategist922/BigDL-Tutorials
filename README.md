# Data Science on Apache Spark

A step-by-step introduction to data science based on Apache Spark and BigDL framework. 

### Topics
1. [RDD](https://github.com/intel-analytics/BigDL-Tutorials/blob/master/notebooks/spark_basics/RDD.ipynb) 
2. [DataFrame](https://github.com/intel-analytics/BigDL-Tutorials/blob/master/notebooks/spark_basics/DataFrame.ipynb)
3. [SparkSQL](https://github.com/intel-analytics/BigDL-Tutorials/blob/master/notebooks/spark_basics/spark_sql.ipynb)
4. [StructureStreaming](https://github.com/intel-analytics/BigDL-Tutorials/blob/master/notebooks/spark_basics/structured_streaming.ipynb)
5. Simple Multiplication
6. [Linear Regression](https://github.com/intel-analytics/BigDL-Tutorials/blob/master/notebooks/neural_networks/linear_regression.ipynb)
7. [Introduction to MNIST](https://github.com/intel-analytics/BigDL-Tutorials/blob/master/notebooks/neural_networks/introduction_to_mnist.ipynb)
8. [Logistic Regression](https://github.com/intel-analytics/BigDL-Tutorials/blob/master/notebooks/neural_networks/logistic_regression.ipynb)
9. [Feedforward Neural Network](https://github.com/intel-analytics/BigDL-Tutorials/blob/master/notebooks/neural_networks/deep_feed_forward_neural_network.ipynb)
10. [Convolutional Neural Network](https://github.com/intel-analytics/BigDL-Tutorials/blob/master/notebooks/neural_networks/cnn.ipynb)
11. [Recurrent Neural Network](https://github.com/intel-analytics/BigDL-Tutorials/blob/master/notebooks/neural_networks/rnn.ipynb)
12. [LSTM](https://github.com/intel-analytics/BigDL-Tutorials/blob/master/notebooks/neural_networks/lstm.ipynb)
13. [Bi-directional RNN](https://github.com/intel-analytics/BigDL-Tutorials/blob/master/notebooks/neural_networks/birnn.ipynb)
14. [Auto-encoder](https://github.com/intel-analytics/BigDL-Tutorials/blob/master/notebooks/neural_networks/autoencoder.ipynb)

### Environment

+ Mac OS/Linux
+ Python 2.7
+ Apache Spark 2.1.0
+ Jupyter Notebook 4.1
+ BigDL ([Linux64](https://repo1.maven.org/maven2/com/intel/analytics/bigdl/dist-spark-2.1.0-scala-2.11.8-linux64/0.1.0/dist-spark-2.1.0-scala-2.11.8-linux64-0.1.0-dist.zip)|[Mac OS](https://repo1.maven.org/maven2/com/intel/analytics/bigdl/dist-spark-2.1.0-scala-2.11.8-mac/0.1.0/dist-spark-2.1.0-scala-2.11.8-mac-0.1.0-dist.zip))

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
