--- 
layout: post
title: Install PostgreSQL on CentOS 5.5
date_pt_BR: 23 JAN 2012
---

#### DISCLAIMER

I did it for 3 times and i always forget the correct way. In case that always that i started installing postgres8.1 on CentOS 5.5, i have got in trouble, anyway, this guide is to remember me 

---

This post will be an express "how to" guide, to install the PostgreSQL on CentOS 5.5.

- First of all, you should install the postgres libs:

  ```sudo yum install postgresql84-server postgresql84-devel```

- After installation concluded, initialize the cluster database:

  ```$ /etc/init.d/postgresql initdb```

- Now start the postres service:
  ```$ /etc/init.d/postgresql start```
  
- And now grab a beer and be happy logged on console:

    ```$ psql -U postgres```

Cheers, bro!
