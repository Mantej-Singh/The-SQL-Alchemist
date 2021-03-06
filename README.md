<p align="center">
  <img src="https://hsto.org/getpro/habr/post_images/44b/d2c/c98/44bd2cc98f2ca6e5d689f21c772ce56e.png">
</p>

# The-Alchemist
SQLAlchemy miniproject


The SQLAlchemy Object Relational Mapper presents a method of associating user-defined Python classes with database tables, and instances of those classes (objects) with rows in their corresponding tables.

[![screenshot_14883s88948.png](https://www.tutorialspoint.com/turbogears/images/orm.jpg)

## Overview:
The SQLAlchemy SQL Toolkit and Object Relational Mapper is a comprehensive set of tools for working with databases and Python. It has several distinct areas of functionality which can be used individually or combined together. Its major components are illustrated below, with component dependencies organized into layers:
[![scrffeenshot_14883s88948.png](http://docs.sqlalchemy.org/en/latest/_images/sqla_arch_small.png)

Above, the two most significant front-facing portions of SQLAlchemy are the Object Relational Mapper and the SQL Expression Language. SQL Expressions can be used independently of the ORM. When using the ORM, the SQL Expression language remains part of the public facing API as it is used within object-relational configurations and queries.
- - - -


## Install via pip
```
pip install SQLAlchemy
```



## Creating Engine
```
from sqlalchemy import create_engine
```


## Connecting with SQLite3
```
db_engine = create_engine('sqlite:///sqlalchemy_example.db')
```
- - - -

# Create a Schema
```
user=Table('users',metadata,
          Column('ID',Integer,primary_key=True),
          Column('name', String(40)),
          Column('age', Integer)
          )
```

          
# output:
[![screenshot-1489115274.png](https://i.postimg.cc/J4kTy75b/screenshot-1489115274.png)](https://postimg.cc/9rcPKhSM)

### Actual Data stored in SQLite db_engine: sqlalchemy_example.db
[![screenshot-1489163026.png](https://i.postimg.cc/xTN4p6QQ/screenshot-1489163026.png)](https://postimg.cc/Mvx5vbX3)

- - - -
- - - -
# Reverse Engineering 

### Create a DataFrame
```
import pandas as pd

col=['ID','Name','Age']

data=[(8,'Ironman',58),
     (9,'Thor',300),
     (10,'Hulk',55)]
     
df=pd.DataFrame(data,columns=col)
```
[![screenshot-1489162928.png](https://i.postimg.cc/qMKCtrkK/screenshot-1489162928.png)](https://postimg.cc/ykVN5w36)

## Output1:
[![screenshot-1489162712.png](https://i.postimg.cc/5NCRKXmR/screenshot-1489162712.png)](https://postimg.cc/qzpwzMSs)

## output2:
[![screenshot-1489162366.png](https://i.postimg.cc/dtT6Bg9R/screenshot-1489162366.png)](https://postimg.cc/BX42ZYkt)

