#.zip
##Packing:

~~~
zip -r foo.zip payload
~~~

##Unpack:

~~~
unzip foo.zip -d ${target path}
~~~

##Peek contents:

~~~
unzip -l foo.zip
~~~

#.tar.gz

##Packing:

~~~
tar zcvf foo.tar.gz payload
~~~

##Unpack:

~~~
tar zxvf foo.tar.gz -C ${target path}
~~~

