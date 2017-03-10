# The-Alchemist
SQLAlchemy miniproject

[![screenshot_1488388948.png](https://hsto.org/getpro/habr/post_images/44b/d2c/c98/44bd2cc98f2ca6e5d689f21c772ce56e.png)


The SQLAlchemy Object Relational Mapper presents a method of associating user-defined Python classes with database tables, and instances of those classes (objects) with rows in their corresponding tables.

[![screenshot_14883s88948.png](https://www.tutorialspoint.com/turbogears/images/orm.jpg)

- - - -




##Creating Engine
```
from sqlalchemy import create_engine
```


##Connecting with SQLite3
```
db_engine = create_engine('sqlite:///sqlalchemy_example.db')
```
- - - -

#Create a Schema
```
db_engine = create_engine('sqlite:///sqlalchemy_example.db')
```
user=Table('users',metadata,
          Column('ID',Integer,primary_key=True),
          Column('name', String(40)),
          Column('age', Integer)
          )
          
#output:
[![screenshot_1489115274.png](https://s19.postimg.org/7c9qtfeb7/screenshot_1489115274.png)](https://postimg.org/image/3snt3mblb/)
