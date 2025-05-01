### 印出link list

+ 假設有一個link list

~~~c
struct list\_entry{
	struct list\_entry *next, prev;
}

struct foo{
  struct list\_entry link;
  uint32\_t payload;
}

struct foo node;
~~~

### cmd
~~~sh
p *(struct foo *)node
$1 = {link={next=0x$nextAddr, prev = 0x$prevAddr}, payload=1}

set $a=(struct foo *)0x$nextAddr
while 1
p *($a)
set $a = (struct foo *)((struct foo *)$a)-\>link.next
end
~~~

or 

~~~sh
set $a=(struct foo *) node.link.next
while 1
p *($a)
set $a=(struct foo *)((struct foo *)$a)-\>link.next
end
~~~
