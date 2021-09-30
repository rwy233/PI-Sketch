## Our Algorithm
Our method of generating apt attack stream is to insert the real apt attack data stream into the normal stream. Because the timestamp intervals of different data streams are different, we shrink the real data stream to make the generated attack stream more reasonable. See gensimdata.cpp for details.
In the data stream we used in the experiment, about 600 attack streams are mixed in hundreds of thousands of normal streams

## how to run
./compile.sh
