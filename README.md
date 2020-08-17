MiniD0S.py - Simple DDOS in Python




What is MiniD0S?



MiniD0S is basically an HTTP Denial of Service attack that affects threaded servers. It works like this:



It will start making lots of HTTP requests.



It will send headers periodically (every ~15 seconds) to keep the connections open


.
It will never close the connection unless the server does so. If the server closes a connection, we create a new one keep doing the same thing.



This exhausts the servers thread pool and the server can't reply to other people.

How to install and run?


You can clone the git repo . Here's how you run it.

git clone https://github.com/allenenosh/minidos

cd minidos

python3 minid0s.py exampletarget.com
