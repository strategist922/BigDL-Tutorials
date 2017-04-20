# BigDL-Tutorials


## Getting Started

### Environment

```
Mac OS Sierra
Python 2.7
Apache Spark 1.4.1
Jupyter Notebook 
```

### Intall Python2.7

Open terminal and type
```
brew install python
```
Check Python version
```
Python --version
```

### Install Apache Spark
Open terminal and type
```
brew install apache-spark
```
### Install Jupyter
Open terminal and type
```
pip install Jupyter
```
### Link Spark with IPython Notebook
Open terminal and type
```
echo "export PATH=$PATH:/usr/local/Cellar/apache-spark/1.4.1/bin" >> .profile
echo "export PYSPARK_DRIVER_PYTHON=ipython" >> .profile
echo "export PYSPARK_DRIVER_PYTHON_OPTS='notebook' pyspark" >> .profile
```
Now you can source it to make changes available in this termial

```
source .profile
```

### Run Jupyter
Open the termial, type `pyspark`. If Spark is correctly linked with Jupyter notebook, the browser should open the Jupyter page. Then open a new notebook, type `sc`. If succeed, you should see something as follows in the screen:

```
In [1]: sc
Out[1]: <pyspark.context.SparkContext at 0x1049bdf90>
```


